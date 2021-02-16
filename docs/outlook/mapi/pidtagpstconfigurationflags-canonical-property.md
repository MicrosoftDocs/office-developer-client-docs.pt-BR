---
title: Propriedade canônica PidTagPstConfigurationFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: e4234ddf-d9dc-4dc9-8eda-dbbee151b5d7
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: e881c8eeffa29706591e07113d70a3670606f2be
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408940"
---
# <a name="pidtagpstconfigurationflags-canonical-property"></a>Propriedade canônica PidTagPstConfigurationFlags
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Especifica sinalizadores de configuração para uma tabela de armazenamento pessoal (arquivo .pst).
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_PST_CONFIG_FLAGS  <br/> |
|Identificador:  <br/> |0x6770  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Tabela de armazenamento pessoal (.pst) interna  <br/> |
   
## <a name="remarks"></a>Comentários

Estes são os valores válidos para essa propriedade:
  
PST_CONFIG_UNICODE
  
> Indica um arquivo .pst Unicode. 
    
   `#define PST_CONFIG_UNICODE 0x80000000`
    
PST_CONFIG_CREATE_NOWARN
  
> Quando definido dos sinalizadores de cliente para o método [IMsgServiceAdmin::ConfigureMsgService,](imsgserviceadmin-configuremsgservice.md) trata **ConfigureMsgService** como uma chamada [de IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) e ignora o aviso "Este serviço de informações não foi configurado". 
    
   `#define PST_CONFIG_CREATE_NOWARN 0x00000001`
    
PST_CONFIG_PRESERVE_DISPLAY_NAME
  
> Informa **ao ConfigureMsgService** para não alterar o valor da propriedade **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), mesmo que ele tenha sido fornecido. Nesse caso, ele foi fornecido apenas para novos arquivos .pst.
    
   `#define PST_CONFIG_PRESERVE_DISPLAY_NAME 0x00000002`
    
OST_CONFIG_POLICY_DELAY_IGNORE_OST
  
> Informa ao código de configuração para exibir primeiro uma caixa de diálogo para confirmar se um arquivo de Pasta Offline (.ost) foi encontrado e, dependendo da resposta do usuário, use a Pasta Offline encontrada ou habilita o usuário a procurar outra Pasta Offline.
    
   `#define OST_CONFIG_POLICY_DELAY_IGNORE_OST 0x00000008`
    
OST_CONFIG_CREATE_NEW_DEFAULT
  
> Copia o arquivo .ost com um novo nome exclusivo e descarta o nome atual. O arquivo .ost existente permanece no computador, mas não é mais usado nesse perfil. Isso normalmente ocorre quando o Microsoft Outlook não permite mais um determinado arquivo .ost, e as políticas do Registro não permitem que o usuário renomeie o arquivo. 
    
   `#define OST_CONFIG_CREATE_NEW_DEFAULT_OST 0x00000010`
    
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]] 
  
> Fornece referências a especificações de protocolo relacionadas do Exchange Server.
    
### <a name="header-files"></a>Arquivos de header

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições de propriedades listadas como propriedades associadas.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapeando nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapeando nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

