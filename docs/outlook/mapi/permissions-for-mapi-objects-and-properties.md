---
title: Permissões para propriedades e objetos MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 32669cbe-5460-4043-99cc-c609608f48da
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 4efa9cd1596cffe19a19a62059f81fa553343d77
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436171"
---
# <a name="permissions-for-mapi-objects-and-properties"></a>Permissões para propriedades e objetos MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
A permissão de acesso, ou o conjunto de operações permissíveis, pode ser uma característica dos objetos MAPI e das propriedades individuais suportadas por esses objetos. O acesso ao objeto é determinado pelo pai de um objeto. Para uma mensagem, sua pasta determina permissões de acesso. Para um usuário de mensagens ou lista de distribuição, seu contêiner de livro de endereços faz essa determinação. Quando um objeto como uma mensagem reside em duas pastas, as permissões para as duas cópias do objeto podem ser diferentes. 
  
Os clientes que usam esses objetos podem solicitar o nível mais alto de acesso permitido para o objeto definindo o sinalizador MAPI_BEST_ACCESS na chamada [IMAPISession::OpenEntry.](imapisession-openentry.md) Dependendo do provedor de serviços que implementa o objeto, o cliente pode ou não ter o nível de acesso necessário. Os clientes podem determinar o nível de acesso ao qual foram concedidos chamando o método **GetProps** do objeto para recuperar a propriedade **PR_ACCESS** ([PidTagAccess).](pidtagaccess-canonical-property.md) No entanto, como o provedor de serviços deve gerar dinamicamente o valor dessa propriedade, é recomendável que os clientes o recuperem somente quando necessário. 
  
Para determinar se um contêiner, como uma pasta, um contêiner de livro de endereços ou uma lista de distribuição permite a modificação, chame seu método **GetProps** para recuperar a propriedade **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)). O acesso ao nível do contêiner afeta os clientes em termos de como eles exibem suas interfaces de usuário. Ele também afeta os implementadores de objetos dentro de contêineres em termos de exibição da interface do usuário e sua implementação geral. 
  
O acesso a uma propriedade específica é determinado pelo esquema de propriedade definido pelo MAPI para o objeto que possui a propriedade. Esquemas de propriedade especificam o conjunto de propriedades obrigatórios e opcionais para um objeto e sua permissão de acesso. Ao contrário do acesso ao objeto que é determinado pelo pai do objeto, o acesso à propriedade é global. Cada objeto, independentemente dos requisitos de acesso do pai do objeto, tem as mesmas permissões para a propriedade conforme determinado pelo esquema.
  
Quando uma propriedade é somente leitura, ela sempre estará disponível com uma **chamada GetProps** ou **OpenProperty.** No entanto, dependendo da implementação do objeto que suporta a propriedade, há dois resultados possíveis para o método **SetProps** para modificar uma propriedade e o **método DeleteProps** para removê-la: 
  
- Falhar e retornar MAPI_E_NO_ACCESS
    
- Êxito sem nenhuma ação tomada
    
O acesso a propriedades e objetos também pode ser recuperado ou definido usando a interface [IPropData](ipropdataimapiprop.md) que herda da interface **IMAPIProp.** MAPI provides an implementation of **IPropData** that is based on data in memory. Os provedores de serviços podem usar **IPropData** para implementar **IMAPIProp** em determinadas circunstâncias, como para seu objeto de status ou se eles estão usando um banco de dados que não tem transações internas. **IPropData** funciona exclusivamente na memória, tornando desnecessário bloquear e desbloquear dados. 
  
## <a name="see-also"></a>Confira também



[Visão geral da propriedade MAPI](mapi-property-overview.md)

