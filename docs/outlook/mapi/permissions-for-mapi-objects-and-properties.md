---
title: Permissões para propriedades e objetos MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 32669cbe-5460-4043-99cc-c609608f48da
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 11c8a58e6cfe0719e8683c4e7a0fd966972117c4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569376"
---
# <a name="permissions-for-mapi-objects-and-properties"></a>Permissões para propriedades e objetos MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Permissão de acesso ou o conjunto de operações permissable, pode ser uma característica de objetos MAPI e das propriedades individuais compatíveis com esses objetos. Acesso do objeto é determinado pelo pai de um objeto. Para uma mensagem, sua pasta determina as permissões de acesso. Para um usuário de mensagens ou lista de distribuição, seu contêiner de catálogo de endereços torna essa determinação. Quando um objeto como uma mensagem reside em duas pastas, as permissões para as duas cópias do objeto podem ser diferentes. 
  
Clientes que usam esses objetos podem solicitar o nível mais alto de acesso permitido para o objeto, definindo o sinalizador MAPI_BEST_ACCESS na chamada [IMAPISession::OpenEntry](imapisession-openentry.md) . Dependendo do provedor de serviço que implementa o objeto, o cliente pode ou não pode ser concedido o nível de acesso necessário. Os clientes podem determinar o nível de acesso que eles foram concedidos chamando o método **GetProps** para recuperar a propriedade **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) do objeto. No entanto, porque o provedor de serviços deve gerar dinamicamente o valor dessa propriedade, é recomendável que os clientes recuperam somente quando necessário. 
  
Para determinar se um recipiente como uma pasta, o contêiner de catálogo de endereços ou lista de distribuição permite a modificação, chame o método **GetProps** para recuperar a propriedade **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)). Nível de acesso do contêiner afeta clientes em termos de como eles serão exibidos suas interfaces do usuário. Ele também afeta os implementadores de objetos dentro de contêineres em termos de sua exibição da interface de usuário e sua implementação geral. 
  
Acesso a uma determinada propriedade é determinado pelo esquema de propriedade configurado pela MAPI para o objeto que possui a propriedade. Esquemas de propriedade especificam o conjunto de propriedades obrigatórios e opcionais para um objeto e seu permissão de acesso. Ao contrário de acesso a objetos que é determinado pelo pai do objeto, o acesso à propriedade é global. Cada objeto, independentemente dos requisitos de acesso de pai do objeto, tem as mesmas permissões para a propriedade conforme determinado pelo esquema.
  
Quando uma propriedade é somente leitura, ele sempre estará disponível com uma chamada **GetProps** ou **OpenProperty** . No entanto, dependendo da implementação do objeto com suporte para a propriedade, existem dois resultados possíveis para o método **SetProps** para modificar uma propriedade e o método **DeleteProps** para removê-lo: 
  
- Falha e retornar MAPI_E_NO_ACCESS
    
- Obtiveram sucesso com nenhuma ação tomada
    
Propriedade e o objeto de acesso também pode ser recuperado ou definido por meio da interface de [IPropData](ipropdataimapiprop.md) herda da interface **IMAPIProp** . MAPI fornece uma implementação do **IPropData** que é baseado em dados na memória. Provedores de serviços podem usar **IPropData** implementar **IMAPIProp** em certas circunstâncias, como para seu objeto de status ou se estiverem usando um banco de dados que não tenha transações internas. **IPropData** funciona exclusivamente na memória, tornando desnecessárias para bloquear e desbloquear dados. 
  
## <a name="see-also"></a>Confira também



[Visão geral da propriedade MAPI](mapi-property-overview.md)

