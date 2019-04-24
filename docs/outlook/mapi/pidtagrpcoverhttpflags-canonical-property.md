---
title: Propriedade canônica PidTagRpcOverHttpFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c8b30768-cf83-450d-9fe2-567a5e0c2f57
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: cf1f3b4d72426fb5f80decdc074a622b140657c8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327444"
---
# <a name="pidtagrpcoverhttpflags-canonical-property"></a>Propriedade canônica PidTagRpcOverHttpFlags

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém as configurações em um perfil usado pelo Microsoft Office Outlook para se conectar ao Microsoft Exchange Server usando uma RPC (chamada de procedimento remoto) sobre protocolo HTTP (Hypertext Transfer Protocol).
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_ROH_FLAGS  <br/> |
|Identificador:  <br/> |0x6623  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Diversos  <br/> |
   
## <a name="remarks"></a>Comentários

A propriedade **PR_ROH_FLAGS** é armazenada na seção de perfil global de um perfil MAPI (Messaging Application Programming Interface). O valor de **PR_ROH_FLAGS** é uma bitmask composta de um ou mais dos seguintes sinalizadores. 
  
|**Nome**|**Valor**|**Descrição**|
|:-----|:-----|:-----|
|**ROHFLAGS_USE_ROH** <br/> |0x1  <br/> |Conecte-se ao servidor Exchange usando RPC sobre HTTP.  <br/> |
|**ROHFLAGS_SSL_ONLY** <br/> |0x2  <br/> |Conecte-se ao Exchange Server usando Secure Socket Layer (SSL) somente.  <br/> |
|**ROHFLAGS_MUTUAL_AUTH** <br/> |0x4  <br/> |Autenticar mutuamente a sessão durante a conexão usando SSL.  <br/> |
|**ROHFLAGS_HTTP_FIRST_ON_FAST** <br/> |0x8  <br/> |Em redes rápidas, conecte-se usando HTTP primeiro. Em seguida, conecte-se usando TCP/IP.  <br/> |
|**ROHFLAGS_HTTP_FIRST_ON_SLOW** <br/> |0x20  <br/> |Em redes lentas, conectar usando HTTP primeiro. Em seguida, conecte-se usando TCP/IP.  <br/> |
   
Por exemplo, para definir a propriedade **PR_ROH_FLAGS** para ativar o RPC sobre http, para exigir SSL e para especificar que o protocolo http deve ser usado primeiro em conexões lentas, defina o valor da propriedade **PR_ROH_FLAGS** como `ROHFLAGS_USE_ROH | ROHFLAGS_SSL_ONLY | ROHFLAGS_HTTP_FIRST_ON_SLOW` sendo igual a 0x23. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações do protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências às especificações relacionadas do protocolo do Exchange Server.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Define as estruturas de dados básicas que são usadas em operações remotas.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica as propriedades e as operações que são permitidas para os objetos de mensagem de email.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs. h
  
> Fornece definições de tipo de dados.
    
Mapitags. h
  
> Contém definições de propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

