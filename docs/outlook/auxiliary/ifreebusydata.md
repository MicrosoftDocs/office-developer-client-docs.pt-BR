---
title: IFreeBusyData
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c9a80ad3-6311-fe07-b6f7-9fd63424753b
ms.openlocfilehash: aa42561277d5fc4de93eeedec8ceb6f36530fb80
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765835"
---
# <a name="ifreebusydata"></a>IFreeBusyData

Para um usuário específico, obtém e define um intervalo de tempo e retorna uma interface para enumerar os blocos de informações de disponibilidade de dados dentro deste intervalo de tempo.
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Herda de:  <br/> |[IUnknown](http://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) <br/> |
|Provided by:  <br/> |Provedor de livre/ocupado  <br/> |
|Identificador de interface:  <br/> |IID_IFreeBusyData  <br/> |
   
## <a name="vtable-order"></a>Ordem vtable

|||
|:-----|:-----|
|[Placeholder1](ifreebusydata-placeholder1.md) <br/> | *Este membro é um espaço reservado e não é suportado.*  <br/> |
|[EnumBlocks](ifreebusydata-enumblocks.md) <br/> |Obtém uma interface que enumera blocos de informações de disponibilidade de dados de um usuário em um intervalo de tempo especificado.  <br/> |
|[Placeholder2](ifreebusydata-placeholder2.md) <br/> | *Este membro é um espaço reservado e não é suportado.*  <br/> |
|[Placeholder3](ifreebusydata-placeholder3.md) <br/> | *Este membro é um espaço reservado e não é suportado.*  <br/> |
|[Placeholder4](ifreebusydata-placeholder4.md) <br/> | *Este membro é um espaço reservado e não é suportado.*  <br/> |
|[Placeholder5](ifreebusydata-placeholder5.md) <br/> | *Este membro é um espaço reservado e não é suportado.*  <br/> |
|[SetFBRange](ifreebusydata-setfbrange.md) <br/> |Define o intervalo de tempo para uma enumeração de blocos de informações de disponibilidade de dados para um usuário.  <br/> |
|[Placeholder6](ifreebusydata-placeholder6.md) <br/> | *Este membro é um espaço reservado e não é suportado.*  <br/> |
|[GetFBPublishRange](ifreebusydata-getfbpublishrange.md) <br/> |Obtém um intervalo de tempo predefinido para uma enumeração de blocos de informações de disponibilidade de dados para um usuário.  <br/> |
   
## <a name="remarks"></a>Coment�rios

A maioria dos membros nessa interface é espaços reservados reservados para uso interno do Outlook e está sujeita a alterações. Provedores de livre/ocupado devem implementá-los conforme especificado, retornando que apenas especificado retorna valores.
  
## <a name="see-also"></a>Confira também

- [Sobre a API do serviço de disponibilidade](about-the-free-busy-api.md)
- [Constantes (API de livre/ocupado)](constants-free-busy-api.md)

