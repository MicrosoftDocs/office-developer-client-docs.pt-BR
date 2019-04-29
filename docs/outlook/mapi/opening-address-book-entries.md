---
title: Abrir entradas do catálogo de endereços
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 017a62c0-49c6-47fb-acce-db58e6bb9cc5
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 6ebd6009700742e9b1159bc95ff0496c423e512c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422156"
---
# <a name="opening-address-book-entries"></a>Abrir entradas do catálogo de endereços

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Quando um cliente ou provedor solicitar que um de seus objetos seja aberto, o MAPI chamará o método [IABLogon:: OpenEntry](iablogon-openentry.md) do provedor. O MAPI determina que o identificador de entrada que representa o objeto de destino pertence ao seu provedor examinando a parte [MAPIUID](mapiuid.md) do identificador de entrada e fazendo a correspondência com o **MAPIUID** que seu provedor registrou na chamada para ** IMAPISupport:: SetProviderUID**. Em seguida, o MAPI chama o método **OpenEntry** . Seu provedor deve responder recuperando o objeto correspondente — um contêiner, uma lista de distribuição ou um usuário de mensagens. 
  
Um identificador de entrada nulo indica uma solicitação para abrir o contêiner raiz do provedor do catálogo de endereços. Os clientes abrem o contêiner raiz para acessar sua tabela de hierarquia e seus destinatários. Os provedores de catálogo de endereços que só fornecem modelos para a criação de destinatários únicos não oferecem suporte à chamada **OpenEntry** para o contêiner raiz. 
  
### <a name="to-implement-iablogonopenentry"></a>Para implementar o IABLogon:: OpenEntry
  
1. Verifique se o identificador de entrada é um identificador válido para o qual seu provedor oferece suporte. Se não for um identificador de entrada válido, retorne MAPI_E_INVALID_ENTRYID. 
    
2. Verifique o sinalizador que é passado com o parâmetro _parâmetroulflags_ . Se o MAPI tiver passado no MAPI_MODIFY e seu provedor não permitir que seus objetos sejam modificados, falhará e retornará o valor de erro MAPI_E_ACCESS_DENIED. 
    
3. Verifique se a interface solicitada no parâmetro _lpInterface_ é válida para o tipo de objeto que seu provedor foi solicitado a abrir. Se um parâmetro inválido tiver sido passado, falhar e retornar o valor de erro MAPI_E_INTERFACE_NOT_SUPPORTED. 
    
4. Se o parâmetro _cbEntryID_ for zero, esta é uma solicitação para abrir o contêiner raiz do provedor. Crie o contêiner raiz e retorne um ponteiro para sua implementação de interface **IABContainer** . 
    
5. Se seu provedor implementar vários objetos de logon, cada um com seu próprio **MAPIUID**registrado, mapeie o **MAPIUID** contido no identificador de entrada com o objeto de logon apropriado. 
    
6. Determine qual tipo de objeto o identificador de entrada representa: um usuário de mensagens, uma lista de distribuição ou um contêiner pertencente ao seu provedor ou um usuário de mensagens única ou uma lista de distribuição para que o valor apropriado possa ser definido para o _lpulObjectType_ Construtor. 
    
7. Crie o objeto do tipo apropriado e defina as seguintes propriedades básicas:
    
    - **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))
    - **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
    - **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))
    - **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
8. Calcule **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) e **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) de informações no identificador de entrada.
    
9. ReTorne um ponteiro para a implementação de interface para o objeto. 
    

