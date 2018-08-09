---
title: Propriedade canônica PidTagObjectType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagObjectType
api_type:
- HeaderDef
ms.assetid: 37da4ff5-300d-479f-a8b4-6fc36df997d9
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 2830da6aad561045a7ecdd953286c90edea88ca2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769522"
---
# <a name="pidtagobjecttype-canonical-property"></a>Propriedade canônica PidTagObjectType

  
  
**Aplica-se a**: Outlook 
  
Contém o tipo de um objeto. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_OBJECT_TYPE  <br/> |
|Identificador:  <br/> |0x0FFE  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Comuns  <br/> |
   
## <a name="remarks"></a>Comentários

O tipo de objeto contido nessa propriedade corresponde à interface principal disponível para um objeto acessível por meio da interface **OpenEntry** . Ele geralmente é obtido consultando o parâmetro _lpulObjType_ retornado pelo método **OpenEntry** apropriado. Quando a interface é obtida de outras maneiras, chame [IMAPIProp::GetProps](imapiprop-getprops.md) para obter o valor dessa propriedade. 
  
Essa propriedade pode ter exatamente um dos seguintes valores:
  
MAPI_ABCONT 
  
> Objeto de contêiner de catálogos de endereços 
    
MAPI_ADDRBOOK 
  
> Objeto de catálogo de endereços 
    
MAPI_ATTACH 
  
> Objeto de anexo de Message 
    
MAPI_DISTLIST 
  
> Objeto de lista de distribuição 
    
MAPI_FOLDER 
  
> Objeto Folder 
    
MAPI_FORMINFO 
  
> Objeto Form 
    
MAPI_MAILUSER 
  
> Objeto de usuário de mensagens 
    
MAPI_MESSAGE 
  
> Objeto de mensagem 
    
MAPI_PROFSECT 
  
> Objeto section de perfil 
    
MAPI_SESSION 
  
> Objeto da sessão 
    
MAPI_STATUS 
  
> Objeto de status 
    
MAPI_STORE 
  
> Objeto de repositório de mensagem
    
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a relacionados especificações de protocolo do Exchange Server.
    
[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Especifica as propriedades e operações para obter listas de usuários, contatos, grupos e recursos.
    
[[MS-NSPI]](http://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)
  
> Trata a comunicação do cliente com um servidor de nome serviço provedor NSPI (Interface).
    
[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> Trata as operações de pasta.
    
[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Trata da ordem e o fluxo para transferências de dados entre um cliente e servidor.
    
[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Converte de convenções de email padrão da Internet para os objetos de mensagem.
    
[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Trata objetos de mensagem e o anexo.
    
[[MS-OXOAB]](http://msdn.microsoft.com/library/b4750386-66ec-4e69-abb6-208dd131c7de%28Office.15%29.aspx)
  
> Especifica os formatos de arquivo do OAB (catálogo) de endereços offline para o cache de objetos do catálogo de endereço local.
    
[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica as propriedades e operações que são permitidas para objetos de mensagem de email.
    
[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)
  
> Especifica as propriedades e operações para a manipulação de uma configuração de lista da pasta de pesquisa.
    
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

