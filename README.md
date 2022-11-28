

# 경고: 아직 개발중인 도구 입니다!!!

## 설명
KCAS, **K**ubernetes **C**cluster **A**uto **S**caler의 약자. 

Kubernetes Federation v2기반으로 클러스터 통합 및 클러스터 스케일 아웃을 지원 합니다. 

동작방식은 기본적으로 IPI(Infrastructure Provider Intergration) 및 Baremetal를 위한 Provisioning를 제공합니다.

프로비저닝을 제공하기 위해서 다음과 같은 표준 도구를 사용합니다.

- pxe
- tftp
- dhcpd
- httpd

클러스터 및 워커 노드에 대한 스케일링 아웃은 아래와 같은 도구로 지원이 됩니다.

- ansible
- kubernetes operator sdk
- duststack-k8s-auto

쿠버네티스 노드 확장을 위한 도구는 아래 저장소의 **앤서블 플레이북**를 사용하고 있습니다.

**확장기능 살펴보기:** [dustbox-k8s-auto](https://github.com/tangt64/duststack-k8s-auto)

KCAS는 Public Cloud Provider가 제공하는 기능과 다릅니다. 쿠버네티스는 "cluster provider"를 통해서 "worker node"확장 기능을 제공하고 있습니다.
KCAS는 동일하게 kubernetes cluster provider와 같은 기능을 제공하지만, 베어메탈 및 ansible API module를 통해서 확장하기 때문에 노드 및 클러스터 확장성에 대한 유연함이 더 높습니다.

## 구조
아직 쿠버네티스 오퍼레이트로 통합은 되지 않았습니다. 구성 요소는 두 가지로 되어 있습니다.

![](http://github.com/tangt64/)