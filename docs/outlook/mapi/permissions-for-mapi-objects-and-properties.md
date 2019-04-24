---
title: Permissões para objetos e propriedades MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 32669cbe-5460-4043-99cc-c609608f48da
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 4efa9cd1596cffe19a19a62059f81fa553343d77
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348591"
---
# <a name="permissions-for-mapi-objects-and-properties"></a>Permissões para objetos e propriedades MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
A permissão de acesso ou o conjunto de operações permissivas pode ser uma característica de objetos MAPI e de propriedades individuais compatíveis com esses objetos. O acesso ao objeto é determinado pelo pai de um objeto. Para uma mensagem, sua pasta determina as permissões de acesso. Para um usuário de mensagens ou lista de distribuição, seu contêiner de catálogo de endereços faz essa determinação. Quando um objeto, como uma mensagem, está em duas pastas, as permissões para as duas cópias do objeto podem ser diferentes. 
  
Os clientes que usam esses objetos podem solicitar o nível mais alto de acesso permitido para o objeto definindo o sinalizador MAPI_BEST_ACCESS na chamada [IMAPISession:: OpenEntry](imapisession-openentry.md) . Dependendo do provedor de serviços que está implementando o objeto, o cliente pode ou não receber o nível de acesso necessário. Os clientes podem determinar o nível de acesso que foram concedidos chamando o método **** GetProps do objeto para recuperar a propriedade **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)). No enTanto, como o provedor de serviços deve gerar dinamicamente o valor para essa propriedade, é recomendável que os clientes a recuperem apenas quando necessário. 
  
Para determinar se um contêiner como uma pasta, um contêiner de catálogo de endereços ou uma lista de distribuição permite a **** modificação, chame o método GetProps para recuperar a propriedade **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)). O acesso no nível do contêiner afeta os clientes em termos de como eles exibem suas interfaces de usuário. Ele também Impacta os implementadores de objetos em contêineres em termos de exibição da interface do usuário e da implementação geral. 
  
O acesso a uma determinada propriedade é determinado pelo esquema de propriedade configurado por MAPI para o objeto que possui a propriedade. Os esquemas de propriedade especificam o conjunto de propriedades obrigatórias e opcionais para um objeto e sua permissão de acesso. Ao contrário do acesso ao objeto, que é determinado pelo pai do objeto, o acesso à propriedade é global. Todos os objetos, independentemente dos requisitos de acesso do pai do objeto, têm as mesmas permissões para a propriedade, conforme determinado pelo esquema.
  
Quando uma propriedade é somente leitura, ela sempre estará disponível com uma chamada getProps ou **OpenProperty** . **** No enTanto, dependendo da implementação do objeto que oferece suporte à propriedade, há dois resultados possíveis para o método setProps para modificar uma propriedade e o método **DeleteProps** para removê-lo: **** 
  
- Falha e retornar MAPI_E_NO_ACCESS
    
- Êxito sem ação tomada
    
A propriedade e o acesso ao objeto também podem ser recuperados ou definidos usando a interface [IPropData](ipropdataimapiprop.md) que herda da interface **IMAPIProp** . O MAPI fornece uma implementação do **IPropData** que se baseia em dados na memória. Os provedores de serviços podem usar o **IPropData** para implementar o **IMAPIProp** em determinadas circunstâncias, como para o objeto de status ou se estiverem usando um banco de dados que não tenha transações internas. O **IPropData** funciona exclusivamente na memória, tornando desnecessária o bloqueio e o desbloqueio dos dados. 
  
## <a name="see-also"></a>Confira também



[Visão geral da propriedade MAPI](mapi-property-overview.md)

