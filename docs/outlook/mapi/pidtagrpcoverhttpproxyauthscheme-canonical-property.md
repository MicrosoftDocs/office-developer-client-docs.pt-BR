---
title: Propriedade canônica PidTagRpcOverHttpProxyAuthScheme
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6da78f1a-6423-460c-b3a9-fd6441df9cef
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: b8c68c2cd34ba037dc725a7d15575159466d8123
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769856"
---
# <a name="pidtagrpcoverhttpproxyauthscheme-canonical-property"></a>Propriedade canônica PidTagRpcOverHttpProxyAuthScheme

  
  
**Aplica-se a**: Outlook 
  
Representa o protocolo de autenticação a ser usado para esse perfil.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_ROH_PROXY_AUTH_SCHEME  <br/> |
|Identificador:  <br/> |0x6627  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Diversos  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade pode ser definida para a autenticação básica ou autenticação NT LAN Manager (NTLM). Os valores possíveis para essa propriedade são os seguintes.
  
|**Name**|**Valor**|**Descrição**|
|:-----|:-----|:-----|
|**ROHAUTH_BASIC** <br/> |0x1  <br/> |Autenticação básica  <br/> |
|**ROHAUTH_NTLM** <br/> |0x2  <br/> |Autenticação NTLM  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a relacionados especificações de protocolo do Exchange Server.
    
[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Define as estruturas de dados básicos que são usadas em operações remotas.
    
[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica as propriedades e operações que são permitidas para objetos de mensagem de email.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições das propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

