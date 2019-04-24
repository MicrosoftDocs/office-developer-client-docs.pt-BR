---
title: Propriedade canônica PidTagRtfSyncBodyCount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRtfSyncBodyCount
api_type:
- COM
ms.assetid: b7267be4-8d5c-4dc7-86b2-651e03e84f9b
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 6f6e687412dfce1e5fcee6b4a4d64f3e5106455f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331252"
---
# <a name="pidtagrtfsyncbodycount-canonical-property"></a>Propriedade canônica PidTagRtfSyncBodyCount

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém uma contagem dos caracteres significativos do texto da mensagem.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_RTF_SYNC_BODY_COUNT  <br/> |
|Identificador:  <br/> |0x1007  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Mensagem MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

A função [RTFSync](rtfsync.md) calcula a contagem de caracteres no texto usando apenas aqueles que ele considera significativos para a mensagem. Por exemplo, alguns espaços em branco e outros caracteres ignoráveis são omitidos da contagem. 
  
Esta propriedade é uma propriedade auxiliar do formato Rich Text (RTF). Essas propriedades são usadas pela função **RTFSync** e não devem ser usadas diretamente por aplicativos cliente. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações do protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências às especificações relacionadas do protocolo do Exchange Server.
    
[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Codifica e decodifica objetos Message e Attachment para uma representação de fluxo eficiente.
    
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

