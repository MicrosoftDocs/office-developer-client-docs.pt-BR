---
title: IEnumFBBlock
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fad9c0fd-b523-db98-ee0d-78aad5914ff2
ms.openlocfilehash: 536c19aa314db9fca39298536c12464e71a71407
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765839"
---
# <a name="ienumfbblock"></a>IEnumFBBlock

Suporta acessando e enumerando blocos de informações de disponibilidade de dados de um usuário em um intervalo de tempo.
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Herda de:  <br/> |[IUnknown](http://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) <br/> |
|Provided by:  <br/> |Provedor de livre/ocupado  <br/> |
|Identificador de interface:  <br/> |**IEnumFBBlock** <br/> |
   
## <a name="vtable-order"></a>Ordem vtable

|||
|:-----|:-----|
|[Next](ienumfbblock-next.md) <br/> |Obtém o próximo número especificado de blocos de informações de disponibilidade de dados em uma enumeração.  <br/> |
|[Ignorar](ienumfbblock-skip.md) <br/> |Ignora um número especificado de blocos de informações de disponibilidade de dados.  <br/> |
|[Reset](ienumfbblock-reset.md) <br/> |Redefine o enumerador, definindo o cursor para o início.  <br/> |
|[Clone](ienumfbblock-clone.md) <br/> |Cria uma cópia do enumerador, usando a mesma restrição de tempo, mas definir o cursor para o início do enumerador.  <br/> |
|[Restringir](ienumfbblock-restrict.md) <br/> |Restringe a enumeração para um período de tempo especificado.  <br/> |
   
## <a name="remarks"></a>Comentários

Uma enumeração contém blocos de informações de disponibilidade de dados que não se sobreponham em tempo. Quando houver sobreposição de itens em um calendário, o Outlook mescla desses itens para formar não sobrepostos blocos de livre/ocupado na enumeração com base nesta ordem de precedência: fora do escritório, ocupado, provisório.
  
Um provedor de livre/ocupado obtém essa interface e a enumeração para um intervalo de tempo para um usuário por meio de [IFreeBusyData](ifreebusydata.md).
  
## <a name="see-also"></a>Confira também

- [Sobre a API do serviço de disponibilidade](about-the-free-busy-api.md)  
- [Constantes (API de livre/ocupado)](constants-free-busy-api.md)  
- [IFreeBusyData](ifreebusydata.md)

