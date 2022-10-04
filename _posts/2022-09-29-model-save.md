---
title: "모델 저장 & 불러오기"
categories:
  - til
tags:
  - pytorch
toc: true
toc_sticky: true
---

## 1. 모델 전체 저장하기
### 1.1 모델 저장하기
- 모델 전체를 저장하면 모델의 계층 구조, 매개변수 등 모든 정보가 기록되어 저장됩니다. 모델 저장을 위해서는 ```torch.save```를 이용합니다.
```python
torch.save(model, PATH)
```
- 이때 모델 파일은 ```*.pt``` 혹은 ```*.pth``` 확장자를 이용해 저장합니다.

### 1.2 모델 불러오기
- 저장한 모델을 불러오기 위해서는 ```torch.load```를 이용합니다.
```python
model = torch.load(PATH)
model.eval()
```
- 추론 결과의 일관성을 위해 ```model.eval()```을 사용한다. ```model.eval()```은 evaluation 과정에서 사용하지 않는 layer들의 전원을 끄는 것이다. [참고 자료](https://stackoverflow.com/questions/60018578/what-does-model-eval-do-in-pytorch/60018731#60018731)

## 2. 모델의 상태만 저장하기
### 2.1 모델 저장하기
- 학습된 모델의 매개변수만 저장할 때는 ```state_dict```를 사용합니다. ```state_dict```는 각 계층의 매개변수(가중치, bias)가 담겨있는 ```dict``` 객체입니다.

- ```state_dict```에은 아래와 같이 ```OrderedDict``` 형태로 layer의 ```weight```와 ```bias```가 저장되어있습니다.
```
OrderedDict(
    [
        (
            'layer1.weight', tensor([[ 0.1473,  0.0778,  0.0134]], device='cuda:0')
        ),
        (
            'layer1.0.bias', tensor([-0.1858,  0.0684], device='cuda:0')
        )
    ]
)
```
- 학습한 결과를 저장하기 위해서는 마찬가지로 ```torch.save()```를 이용합니다.
```python
torch.save(model.state_dict(), PATH)
```
### 2.2 모델 불러오기
- 모델을 불러올 때는 ```torch.load()```와 ```load_state_dict()```을 이용합니다.
```python
model.load_state_dict(torch.load(PATH))
model.eval()
```

## 3. checkpoint
- 체크포인트는 학습 과정 중 일정 ```epoch```마다 결과를 저장하여 나중에 이어서 학습할 수 있도록 하는 것입니다. 체크포인트를 통해 중간에 학습이 중단될 경우를 방지할 수 있습니다.
### 3.1 체크포인트 저장하기
- 학습 재개를 위해 체크포인트를 저장할 때는 ```optimizer```의 ```state_dict```, 마지막 ```epoch```, ```loss``` 등을 추가로 저장해야합니다.
```python
torch.save({
    'epoch': epoch,
    'model_state_dict': model.state_dict(),
    'optimazer_state_dict': optimazer.state_dict(),
    'loss': loss,
    ...
}, PATH)
```

### 3.1 체크포인트 불러오기
- 체크포인트 항목들을 불러올 때는 ```torch.load()```를 이용해 불러옵니다.
```python
checkpoint = torch.load(PATH)
model.load_state_dict(checkpoint['model_state_dict'])
optimazer.load_state_dict(checkpoint['optimizer_state_dict'])
epoch = checkpoint['epoch']
loss = checkpoint['loss']
```

## 참고 자료
- [Python Pytorch 강좌 : 제 10강 - 모델 저장/불러오기(Model Save/Load)](https://076923.github.io/posts/Python-pytorch-10/)
- [모델 저장하기 & 불러오기](https://tutorials.pytorch.kr/beginner/saving_loading_models.html#inference)