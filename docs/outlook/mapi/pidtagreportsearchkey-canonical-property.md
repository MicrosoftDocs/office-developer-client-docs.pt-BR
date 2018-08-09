---
title: Propriedade canônica PidTagReportSearchKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReportSearchKey
api_type:
- COM
ms.assetid: d4f4c40b-b6a8-45f3-b750-07b92c535322
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: fa2770daf38fe93eb9fb69990eebc2a6fcfd6a27
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769848"
---
# <a name="pidtagreportsearchkey-canonical-property"></a>Propriedade canônica PidTagReportSearchKey

  
  
**Aplica-se a**: Outlook 
  
Contém a chave de pesquisa para o destinatário que deve obter relatórios para esta mensagem.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_REPORT_SEARCH_KEY  <br/> |
|Identificador:  <br/> |0x0054  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Envelope MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade é uma das propriedades de endereço do destinatário que o remetente tenha delegada para receber qualquer relatórios gerados para esta mensagem.
  
Um aplicativo cliente que deve rotear relatórios para outro usuário deverá definir essa propriedade em tempo de envio de mensagem. Se não estiver definida, os relatórios são enviados para o remetente da mensagem.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a relacionados especificações de protocolo do Exchange Server.
    
[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica as propriedades e operações que são permitidas em mensagens de email.
    
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

