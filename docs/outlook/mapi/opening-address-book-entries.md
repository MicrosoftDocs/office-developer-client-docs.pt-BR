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
  
Quando um cliente ou provedor solicitou que um de seus objetos seja aberto, o MAPI chama o método [IABLogon::OpenEntry do](iablogon-openentry.md) provedor. O MAPI determina que o identificador de entrada que representa o objeto de destino pertence ao seu provedor examinando a parte [MAPIUID](mapiuid.md) do identificador de entrada e correspondendo-o ao **MAPIUID** que seu provedor registrou na chamada para **IMAPISupport::SetProviderUID**. MAPI then calls your **OpenEntry** method. Seu provedor deve responder recuperando o objeto correspondente — um contêiner, uma lista de distribuição ou um usuário de mensagens. 
  
Um identificador de entrada NULL indica uma solicitação para abrir o contêiner raiz do provedor de agendas. Os clientes abrem o contêiner raiz para acessar sua tabela de hierarquia e seus destinatários. Os provedores de agendamento de endereços que fornecem apenas modelos para a criação de destinatários únicos não suportam a chamada **OpenEntry** para o contêiner raiz. 
  
### <a name="to-implement-iablogonopenentry"></a>Para implementar IABLogon::OpenEntry
  
1. Verifique se o identificador de entrada é um identificador válido compatível com seu provedor. Se não for um identificador de entrada válido, retorne MAPI_E_INVALID_ENTRYID. 
    
2. Verifique o sinalizador que é passado com o _parâmetro ulFlags._ Se o MAPI tiver passado pelo MAPI_MODIFY e seu provedor não permitir que seus objetos sejam modificados, falhará e retornará o MAPI_E_ACCESS_DENIED de erro. 
    
3. Verifique se a interface solicitada no parâmetro  _lpInterface_ é válida para o tipo de objeto que seu provedor foi solicitado a abrir. Se um parâmetro inválido tiver sido passado, falhará e retornará o valor MAPI_E_INTERFACE_NOT_SUPPORTED erro. 
    
4. Se o  _parâmetro cbEntryID_ for zero, será uma solicitação para abrir o contêiner raiz do provedor. Crie o contêiner raiz e retorne um ponteiro para sua implementação de interface **IABContainer.** 
    
5. Se seu provedor implementa vários objetos de logon, cada um com seu próprio **MAPIUID** registrado, mapeie o **MAPIUID** contido no identificador de entrada com o objeto de logon apropriado. 
    
6. Determine que tipo de objeto o identificador de entrada representa: um usuário de mensagens, uma lista de distribuição ou um contêiner pertencente ao seu provedor ou um usuário de mensagens único ou uma lista de distribuição para que o valor apropriado possa ser definido para o parâmetro _lpulObjectType._ 
    
7. Criar o objeto do tipo apropriado e definir as seguintes propriedades básicas:
    
    - **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))
    - **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
    - **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))
    - **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
8. Calcule **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) e **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) de informações no identificador de entrada.
    
9. Retorne um ponteiro para a implementação da interface do objeto. 
    

