---
title: IEnumFBBlock
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fad9c0fd-b523-db98-ee0d-78aad5914ff2
ms.openlocfilehash: 2b37aa2000218acc0663ee8e2db12f01b93c0663
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317623"
---
# <a name="ienumfbblock"></a>IEnumFBBlock

Oferece suporte ao acesso e enumeração de blocos de disponibilidade de dados de um usuário em um intervalo de tempo.
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Herda de:  <br/> |[IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) <br/> |
|Fornecido por:  <br/> |Provedor de disponibilidade  <br/> |
|Identificador de interface:  <br/> |**IEnumFBBlock** <br/> |
   
## <a name="vtable-order"></a>Vtable order

|||
|:-----|:-----|
|[Next](ienumfbblock-next.md) <br/> |Obtém o próximo número específico de blocos de disponibilidade de dados em uma enumeração.  <br/> |
|[Skip](ienumfbblock-skip.md) <br/> |Pula um número específico de blocos de disponibilidade de dados.  <br/> |
|[Reset](ienumfbblock-reset.md) <br/> |Redefine o enumerador configurando o cursor para o início.  <br/> |
|[Clone](ienumfbblock-clone.md) <br/> |Cria uma cópia do enumerador, usando a mesma restrição de tempo, mas definindo o cursor para o início do enumerador.  <br/> |
|[Restrict](ienumfbblock-restrict.md) <br/> |Restringe a enumeração para um período específico.  <br/> |
   
## <a name="remarks"></a>Comentários

Uma enumeração contém blocos disponibilidade de dados que não ficam sobrepostos no período. Quando há itens sobrepostos em um calendário, o Outlook mescla esses itens para formar blocos de disponibilidade não sobrepostos na enumeração com base nesta ordem de prioridade: ausência temporária, ocupado, provisório.
  
Um provedor de disponibilidade obtém essa interface e a enumeração em um intervalo de tempo para o usuário por meio de [IFreeBusyData](ifreebusydata.md).
  
## <a name="see-also"></a>Confira também

- [Sobre a API do serviço de disponibilidade](about-the-free-busy-api.md)  
- [Constantes (API do serviço de disponibilidade)](constants-free-busy-api.md)  
- [IFreeBusyData](ifreebusydata.md)

