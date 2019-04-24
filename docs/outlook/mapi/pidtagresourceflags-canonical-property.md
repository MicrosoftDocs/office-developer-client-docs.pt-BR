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
ms.openlocfilehash: 2fb9eed0beaf7269ac90a021dae650355484ebc2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330181"
---
# <a name="pidtagresourceflags-canonical-property"></a>Propriedade canônica PidTagResourceFlags

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém uma bitmask de sinalizadores para serviços de mensagens e provedores.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_RESOURCE_FLAGS  <br/> |
|Identificador:  <br/> |0x3009  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |MAPI comum  <br/> |
   
## <a name="remarks"></a>Comentários

Esta propriedade descreve as características de um serviço de mensagens, um provedor de serviços ou um objeto status. Os sinalizadores definidos para esta propriedade dependem do seu contexto. Por exemplo, alguns sinalizadores são válidos somente para objetos status e outros sinalizadores somente para colunas na tabela de serviço de mensagens. 
  
Os sinalizadores são de três classes: estática, modificável e dinâmica. Os sinalizadores estáticos são definidos por MAPI de dados em MAPISVC. INF e nunca alterado. Os sinalizadores modificáveis são definidos por MAPI de MAPISVC. INF, mas pode ser alterado subsequentemente. Sinalizadores dinâmicos podem ser definidos e redefinidos por métodos MAPI.
  
Para um serviço de mensagens, um ou mais dos seguintes sinalizadores podem ser definidos nesta propriedade:
  
SERVICE_CREATE_WITH_STORE 
  
> Reservado. Não usar.
    
SERVICE_DEFAULT_STORE 
  
> Dinâmica. O serviço de mensagens contém o repositório padrão. Uma interface do usuário deve ser exibida solicitando a confirmação do usuário antes de excluir ou mover esse serviço do perfil. 
    
SERVICE_NO_PRIMARY_IDENTITY 
  
> Estatistica. O sinalizador de nível de serviço que deve ser definido para indicar que nenhum dos provedores no serviço de mensagens pode ser usado para fornecer uma identidade. Este sinalizador ou SERVICE_PRIMARY_IDENTITY deve ser definido, mas não ambos.
    
SERVICE_PRIMARY_IDENTITY 
  
> Modificável. O serviço de mensagens correspondente contém o provedor usado para a identidade principal desta sessão. Use [IMsgServiceAdmin:: SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md) para definir esse sinalizador. Este sinalizador ou SERVICE_NO_PRIMARY_IDENTITY deve ser definido, mas não ambos. 
    
SERVICE_SINGLE_COPY 
  
> Estatistica. Qualquer tentativa de criar ou copiar esse serviço de mensagens em um perfil onde o serviço já existe falhará. Para criar um serviço de mensagem de cópia única, adicione a propriedade **PR_RESOURCE_FLAGS** à seção do serviço em MAPISVC. INF e defina esse sinalizador. 
    
Para um provedor de serviços, um ou mais dos seguintes sinalizadores podem ser definidos no **PR_RESOURCE_FLAGS**:
  
HOOK_INBOUND 
  
> Estatistica. O gancho do spooler precisa processar mensagens de entrada.
    
HOOK_OUTBOUND 
  
> Estatistica. O gancho do spooler precisa processar mensagens de saída. 
    
STATUS_DEFAULT_OUTBOUND 
  
> Modificável. Essa identidade deve ser aplicada a mensagens de saída se o perfil contiver várias instâncias desse provedor de transporte. Isso pode acontecer se várias instâncias de um único provedor de transporte aparecerem no perfil.
    
STATUS_DEFAULT_STORE 
  
> Modificável. Este repositório de mensagens é o repositório padrão para o perfil. 
    
STATUS_NEED_IPM_TREE 
  
> Dinâmica. As pastas padrão neste repositório de mensagens, incluindo a pasta raiz da mensagem interpessoal (IPM), ainda não foram verificadas. MAPI define e limpa esse sinalizador. 
    
STATUS_NO_DEFAULT_STORE 
  
> Estatistica. Este repositório de mensagens é incapaz de se tornar o repositório de mensagens padrão para o perfil.
    
STATUS_NO_PRIMARY_IDENTITY 
  
> Estatistica. Esse provedor não fornece uma identidade na linha de status. Este sinalizador ou STATUS_PRIMARY_IDENTITY deve ser definido.
    
STATUS_OWN_STORE 
  
> Estatistica. Esse provedor de transporte está rigidamente acoplado a um repositório de mensagens e fornece a propriedade **PR_OWN_STORE_ENTRYID** ([PidTagOwnStoreEntryId](pidtagownstoreentryid-canonical-property.md)) em sua linha de status.
    
STATUS_PRIMARY_IDENTITY 
  
> Modificável. Este provedor fornece a identidade principal para a sessão; o identificador de entrada para o objeto que fornece a identidade é retornado de [IMAPISession:: QueryIdentity](imapisession-queryidentity.md). Este sinalizador ou **STATUS_NO_PRIMARY_IDENTITY** deve ser definido. 
    
STATUS_PRIMARY_STORE 
  
> Modificável. Este repositório de mensagens deve ser usado quando um aplicativo cliente faz logon. Depois de aberto, esse repositório deverá ser definido como o repositório padrão para o perfil. 
    
STATUS_SECONDARY_STORE 
  
> Modificável. Este repositório de mensagens será usado se o armazenamento principal não estiver disponível quando um aplicativo cliente fizer logon. Depois de aberto, esse repositório deverá ser definido como o repositório padrão para o perfil. 
    
STATUS_SIMPLE_STORE 
  
> Dinâmica. Este repositório de mensagens será usado pelo Simple MAPI como o seu repositório de mensagens padrão.
    
STATUS_TEMP_SECTION 
  
> Dinâmica. Este repositório de mensagens não deve ser publicado na tabela de repositório de mensagens e será excluído do perfil após o logoff. 
    
STATUS_XP_PREFER_LAST 
  
> Estatistica. Esse transporte espera ser o último transporte selecionado para enviar uma mensagem quando vários provedores de transporte podem transmitir a mensagem.
    
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs. h
  
> Fornece definições de tipo de dados.
    
Mapitags. h
  
> Contém definições de propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md)
  
[Propriedade canônica PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md)


[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

