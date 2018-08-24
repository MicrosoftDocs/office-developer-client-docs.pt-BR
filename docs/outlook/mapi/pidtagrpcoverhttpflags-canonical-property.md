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
ms.openlocfilehash: b36f71958528b25829b1ff85b29572b3590f9d4f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594814"
---
# <a name="pidtagrpcoverhttpflags-canonical-property"></a>Propriedade canônica PidTagRpcOverHttpFlags

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém as configurações em um perfil usado pelo Microsoft Office Outlook para se conectar ao Microsoft Exchange Server usando uma chamada de procedimento remoto (RPC) sobre HTTP (Hypertext Transfer Protocol).
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_ROH_FLAGS  <br/> |
|Identificador:  <br/> |0x6623  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Diversos  <br/> |
   
## <a name="remarks"></a>Comentários

A propriedade **PR_ROH_FLAGS** é armazenada na seção perfil Global de um perfil de Messaging Application Programming Interface (MAPI). O valor de **PR_ROH_FLAGS** é uma bitmask que é composta de um ou mais dos seguintes sinalizadores. 
  
|**Name**|**Valor**|**Descrição**|
|:-----|:-----|:-----|
|**ROHFLAGS_USE_ROH** <br/> |0x1  <br/> |Conecte-se ao servidor do Exchange usando RPC sobre HTTP.  <br/> |
|**ROHFLAGS_SSL_ONLY** <br/> |0x2  <br/> |Conecte-se ao servidor do Exchange usando apenas o Secure Socket Layer (SSL).  <br/> |
|**ROHFLAGS_MUTUAL_AUTH** <br/> |0x4  <br/> |Autenticar mutuamente a sessão durante a conexão usando SSL.  <br/> |
|**ROHFLAGS_HTTP_FIRST_ON_FAST** <br/> |0x8  <br/> |Em redes rápidas, conecte usando HTTP primeiro. Em seguida, conecte usando TCP/IP.  <br/> |
|**ROHFLAGS_HTTP_FIRST_ON_SLOW** <br/> |0x20  <br/> |Em redes lentas, conecte usando HTTP primeiro. Em seguida, conecte usando TCP/IP.  <br/> |
   
Por exemplo, para definir o **PR_ROH_FLAGS** propriedade ativem RPC sobre HTTP, para exigir SSL e para especificar que o protocolo HTTP deve ser usado pela primeira vez em conexões lentas, defina o valor da propriedade **PR_ROH_FLAGS** como `ROHFLAGS_USE_ROH | ROHFLAGS_SSL_ONLY | ROHFLAGS_HTTP_FIRST_ON_SLOW` que é igual a 0x23. 
  
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

