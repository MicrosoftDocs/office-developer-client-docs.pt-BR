---
title: Entradas do catálogo de endereços de abertura
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 017a62c0-49c6-47fb-acce-db58e6bb9cc5
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: c36c70eacffcb4a41af0e73eea85143ab737867f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768187"
---
# <a name="opening-address-book-entries"></a>Entradas do catálogo de endereços de abertura

**Aplica-se a**: Outlook 
  
Quando um cliente ou provedor solicitou que um dos seus objetos seja aberto, MAPI chama o método de [IABLogon::OpenEntry](iablogon-openentry.md) do seu provedor. MAPI determina que o identificador de entrada que representa o objeto de destino pertence ao seu provedor examinando a parte [MAPIUID](mapiuid.md) do identificador de entrada e estabelecendo uma correspondência para o seu provedor registrado na chamada a ** **MAPIUID** IMAPISupport::SetProviderUID**. MAPI chama seu método **OpenEntry** . Seu provedor deve responder recuperando o objeto correspondente — um contêiner, lista de distribuição ou mensagens de usuário. 
  
Um identificador de entrada NULL indica uma solicitação para abrir o contêiner de raiz do provedor de catálogo de endereços. Clientes abrem o contêiner de raiz para acessar sua tabela de hierarquia e seus destinatários. Provedores de catálogo de endereços que apenas forneçam modelos para criação de destinatários únicos não têm suporte para a chamada **OpenEntry** para o contêiner de raiz. 
  
### <a name="to-implement-iablogonopenentry"></a>Para implementar IABLogon::OpenEntry
  
1. Verifique se o identificador de entrada é um identificador válido que o provedor oferece suporte. Se ele não é um identificador de entrada válida, retorne MAPI_E_INVALID_ENTRYID. 
    
2. Verifique se o sinalizador que é passado com o parâmetro _ulFlags_ . Se o MAPI passou no MAPI_MODIFY e seu provedor não permite que seus objetos a ser modificada, falhar e retornar o valor de erro MAPI_E_ACCESS_DENIED. 
    
3. Verifique se a interface solicitada no parâmetro _lpInterface_ é válida para o tipo de objeto que foi solicitado para abrir seu provedor. Se um parâmetro inválido foi passado na, falhar e retornar o valor de erro MAPI_E_INTERFACE_NOT_SUPPORTED. 
    
4. Se o parâmetro _cbEntryID_ for zero, essa é uma solicitação para abrir o contêiner de raiz do seu provedor. Criar o contêiner de raiz e retornar um ponteiro para sua implementação de interface **IABContainer** . 
    
5. Se seu provedor implementa vários objetos de logon, cada um com seu próprio registrado **MAPIUID**, mapa a **MAPIUID** contidos no identificador de entrada com o objeto de logon adequada. 
    
6. Determinar o identificador de entrada de qual tipo de objeto representa: um usuário, lista de distribuição ou contêiner pertencente ao seu provedor ou uma lista de distribuição ou usuário mensagens único para que o valor apropriado pode ser definido para o _lpulObjectType_ mensagens Use o parâmetro. 
    
7. Criar o objeto do tipo apropriado e defina as seguintes propriedades básicas:
    
    - **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))
    - **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
    - **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))
    - **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
8. Calcule **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) e **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) das informações do identificador de entrada.
    
9. Retorne um ponteiro para a implementação de interface para o objeto. 
    

