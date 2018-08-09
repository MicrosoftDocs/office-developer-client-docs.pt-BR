---
title: Propriedade canônica PidTagResourceFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagResourceFlags
api_type:
- COM
ms.assetid: 69be9ad3-006a-459e-9cd4-eb3f609d71ad
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: dae917b3e536aee5f24879edc3ccf0736e7c9f34
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769845"
---
# <a name="pidtagresourceflags-canonical-property"></a>Propriedade canônica PidTagResourceFlags

  
  
**Aplica-se a**: Outlook 
  
Contém uma bitmask dos sinalizadores para serviços de mensagem e provedores.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_RESOURCE_FLAGS  <br/> |
|Identificador:  <br/> |0x3009  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |MAPI comuns  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade descreve as características de um serviço de mensagem, um provedor de serviço ou um objeto de status. Os sinalizadores que estão definidos para esta propriedade dependem de seu contexto. Por exemplo, alguns sinalizadores são válidos somente para objetos de status e outros sinalizadores apenas para colunas na tabela de serviço de mensagem. 
  
Os sinalizadores são das três classes: modificável, estática e dinâmica. Sinalizadores estáticos são definidos por MAPI de dados no MAPISVC. INF e nunca alteradas. Sinalizadores modificáveis são definidos por MAPI do MAPISVC. INF, mas pode ser alterada posteriormente. Sinalizadores dinâmicos podem ser definidas e redefinir pelos métodos MAPI.
  
Para um serviço de mensagem, um ou mais dos seguintes sinalizadores podem ser definido nessa propriedade:
  
SERVICE_CREATE_WITH_STORE 
  
> Reservado. Não a use.
    
SERVICE_DEFAULT_STORE 
  
> Dinâmico. O serviço de mensagem contém o repositório padrão. Uma interface do usuário deve ser exibida, solicitar a confirmação antes de excluir ou mover este serviço de perfil de usuário. 
    
SERVICE_NO_PRIMARY_IDENTITY 
  
> Estático. O sinalizador nível de serviço que deve ser definido para indicar que nenhum dos provedores no serviço de mensagem pode ser usada para fornecer uma identidade. Este sinalizador ou SERVICE_PRIMARY_IDENTITY deve ser definido, mas não ambos.
    
SERVICE_PRIMARY_IDENTITY 
  
> Pode ser modificado. O serviço correspondente da mensagem contém o provedor usado para a identidade principal nesta sessão. Use [IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md) para definir esse sinalizador. Este sinalizador ou SERVICE_NO_PRIMARY_IDENTITY deve ser definido, mas não ambos. 
    
SERVICE_SINGLE_COPY 
  
> Estático. Qualquer tentativa de criar ou copiar esse serviço de mensagem para um perfil de onde o serviço já existe falhará. Para criar uma única cópia o serviço de mensagem adicionar a propriedade **PR_RESOURCE_FLAGS** à seção do serviço em MAPISVC. INF e definir esse sinalizador. 
    
Para um provedor de serviço, um ou mais dos seguintes sinalizadores podem ser definido em **PR_RESOURCE_FLAGS**:
  
HOOK_INBOUND 
  
> Estático. O gancho spooler deve processar mensagens de entrada.
    
HOOK_OUTBOUND 
  
> Estático. O gancho spooler deve processar mensagens de saída. 
    
STATUS_DEFAULT_OUTBOUND 
  
> Pode ser modificado. Essa identidade deve ser aplicada às mensagens de saída, se o perfil contiver várias instâncias desse provedor de transporte. Isso pode acontecer se várias instâncias de um provedor de transporte único aparecem no perfil.
    
STATUS_DEFAULT_STORE 
  
> Pode ser modificado. Este armazenamento de mensagem é o padrão para o perfil. 
    
STATUS_NEED_IPM_TREE 
  
> Dinâmico. As pastas padrão no armazenamento de mensagens, incluindo a pasta raiz de mensagem interpessoais (IPM), ainda não foi verificadas. Define e limpa esse sinalizador MAPI. 
    
STATUS_NO_DEFAULT_STORE 
  
> Estático. Este armazenamento de mensagens não é capaz de se tornando o armazenamento de mensagens para o perfil padrão.
    
STATUS_NO_PRIMARY_IDENTITY 
  
> Estático. Esse provedor não forneça uma identidade em sua linha de status. Este sinalizador ou STATUS_PRIMARY_IDENTITY deve ser definida.
    
STATUS_OWN_STORE 
  
> Estático. Esse provedor de transporte está firmemente combinado com um armazenamento de mensagens e fornece a propriedade **PR_OWN_STORE_ENTRYID** ([PidTagOwnStoreEntryId](pidtagownstoreentryid-canonical-property.md)) em sua linha de status.
    
STATUS_PRIMARY_IDENTITY 
  
> Pode ser modificado. Esse provedor representa a identidade principal para a sessão; o identificador de entrada para o objeto que forneçam a identidade é retornado por [IMAPISession::QueryIdentity](imapisession-queryidentity.md). Este sinalizador ou **STATUS_NO_PRIMARY_IDENTITY** deve ser definida. 
    
STATUS_PRIMARY_STORE 
  
> Pode ser modificado. Este armazenamento de mensagens deve ser usado quando um aplicativo cliente fizer logon. Uma vez aberto, esse repositório deve ser definido como o repositório padrão para o perfil. 
    
STATUS_SECONDARY_STORE 
  
> Pode ser modificado. Este armazenamento de mensagens deve ser usado se o repositório principal não está disponível quando um aplicativo cliente fizer logon. Uma vez aberto, esse repositório deve ser definido como o repositório padrão para o perfil. 
    
STATUS_SIMPLE_STORE 
  
> Dinâmico. Este armazenamento de mensagens será usado pelo MAPI simples como seu armazenamento de mensagens padrão.
    
STATUS_TEMP_SECTION 
  
> Dinâmico. Este armazenamento de mensagens não deve ser publicado na tabela de repositório de mensagens e será excluído do perfil após o logoff. 
    
STATUS_XP_PREFER_LAST 
  
> Estático. Espera-se que seja o último transporte selecionado para enviar uma mensagem quando vários provedores de transporte são capazes de transmitir a mensagem deste transporte.
    
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições das propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md)
  
[Propriedade canônica PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md)


[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

