---
title: IFreeBusyData
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c9a80ad3-6311-fe07-b6f7-9fd63424753b
ms.openlocfilehash: cd9d4dffd83e1995319b0f0d661435fedb78f28c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393205"
---
# <a name="ifreebusydata"></a>IFreeBusyData

Para um usuário específico, obtém e define um intervalo de tempo e retorna uma interface para enumerar blocos de disponibilidade de dados nesse intervalo de tempo.
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Herda de:  <br/> |[IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) <br/> |
|Fornecido por:  <br/> |Provedor de disponibilidade  <br/> |
|Identificador de interface:  <br/> |IID_IFreeBusyData  <br/> |
   
## <a name="vtable-order"></a>Vtable order

|||
|:-----|:-----|
|[Placeholder1](ifreebusydata-placeholder1.md) <br/> | *Esse membro é um espaço reservado e não tem suporte.*  <br/> |
|[EnumBlocks](ifreebusydata-enumblocks.md) <br/> |É uma interface que enumera blocos de disponibilidade de dados de um usuário em um intervalo de tempo específico.  <br/> |
|[Placeholder2](ifreebusydata-placeholder2.md) <br/> | *Esse membro é um espaço reservado e não tem suporte.*  <br/> |
|[Placeholder3](ifreebusydata-placeholder3.md) <br/> | *Esse membro é um espaço reservado e não tem suporte.*  <br/> |
|[Placeholder4](ifreebusydata-placeholder4.md) <br/> | *Esse membro é um espaço reservado e não tem suporte.*  <br/> |
|[Placeholder5](ifreebusydata-placeholder5.md) <br/> | *Esse membro é um espaço reservado e não tem suporte.*  <br/> |
|[SetFBRange](ifreebusydata-setfbrange.md) <br/> |Define o intervalo de tempo para uma enumeração de blocos de disponibilidade de dados de um usuário.  <br/> |
|[Placeholder6](ifreebusydata-placeholder6.md) <br/> | *Esse membro é um espaço reservado e não tem suporte.*  <br/> |
|[GetFBPublishRange](ifreebusydata-getfbpublishrange.md) <br/> |Obtém um intervalo de tempo pré-definido para uma enumeração de blocos de disponibilidade de dados de um usuário.  <br/> |
   
## <a name="remarks"></a>Comentários

A maioria dos membros dessa interface consiste em espaços reservados para uso interno do Outlook e está sujeita a alterações. Os provedores de disponibilidade devem implementá-los apenas conforme especificado, retornando somente os valores de retorno especificados.
  
## <a name="see-also"></a>Confira também

- [Sobre a API do serviço de disponibilidade](about-the-free-busy-api.md)
- [Constantes (API do serviço de disponibilidade)](constants-free-busy-api.md)

