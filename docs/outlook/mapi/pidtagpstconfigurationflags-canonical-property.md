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
ms.openlocfilehash: b5a3978741f7ecb871e3c3de28e52dffdcf3a74f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769713"
---
# <a name="pidtagpstconfigurationflags-canonical-property"></a>Propriedade canônica PidTagPstConfigurationFlags
  
**Aplica-se a**: Outlook 
  
Especifica os sinalizadores de configuração para uma tabela de armazenamento pessoal (arquivo. pst).
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_PST_CONFIG_FLAGS  <br/> |
|Identificador:  <br/> |0x6770  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Tabela de armazenamento pessoal (. pst) interna  <br/> |
   
## <a name="remarks"></a>Comentários

A seguir estão os valores válidos para essa propriedade:
  
PST_CONFIG_UNICODE
  
> Indica um arquivo. pst de Unicode. 
    
   `#define PST_CONFIG_UNICODE 0x80000000`
    
PST_CONFIG_CREATE_NOWARN
  
> Quando o conjunto do cliente sinalizadores para o método [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) , **ConfigureMsgService** a tratará como uma chamada de [IMsgServiceAdmin:: CreateMsgService](imsgserviceadmin-createmsgservice.md) e ignora a "Este serviço de informações não foi configurado" aviso. 
    
   `#define PST_CONFIG_CREATE_NOWARN 0x00000001`
    
PST_CONFIG_PRESERVE_DISPLAY_NAME
  
> Informa **ConfigureMsgService** não alterar o valor da propriedade **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), mesmo que ele foi fornecido. Nesse caso, ele foi fornecido apenas para os novos arquivos. pst.
    
   `#define PST_CONFIG_PRESERVE_DISPLAY_NAME 0x00000002`
    
OST_CONFIG_POLICY_DELAY_IGNORE_OST
  
> Informa o código de configuração para o primeiro exibir uma caixa de diálogo para confirmar se um arquivo de pasta Offline (. ost) foi encontrado e, dependendo da resposta do usuário, usar a pasta Offline encontrado ou permitir que o usuário navegue para outra pasta Offline.
    
   `#define OST_CONFIG_POLICY_DELAY_IGNORE_OST 0x00000008`
    
OST_CONFIG_CREATE_NEW_DEFAULT
  
> Copia o arquivo. ost com um novo nome exclusivo e descarta o nome atual. O arquivo. ost existente permanece no computador, mas não é mais usado neste perfil. Normalmente, isso ocorre quando o Microsoft Outlook não são mais permite que um arquivo. ost específico e políticas de registro não permitir que o usuário renomeie o arquivo. 
    
   `#define OST_CONFIG_CREATE_NEW_DEFAULT_OST 0x00000010`
    
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]] 
  
> Fornece referências a relacionados especificações de protocolo do Exchange Server.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições das propriedades listadas como propriedades associadas.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

