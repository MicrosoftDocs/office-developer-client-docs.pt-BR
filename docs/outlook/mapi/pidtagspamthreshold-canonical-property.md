---
title: Propriedade canônica PidTagSpamThreshold
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2b2d6b8e-e3dd-4a9b-8bb5-53add675605d
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 24a033269b072712fea6e9957d0ffac3573ce3a1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770042"
---
# <a name="pidtagspamthreshold-canonical-property"></a>Propriedade canônica PidTagSpamThreshold

  
  
**Aplica-se a**: Outlook 
  
Um valor long que indica o nível de filtragem de spam.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_SPAM_THRESHOLD  <br/> |
|ID de longo (LID):  <br/> | 0x041B  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Spam  <br/> |
   
## <a name="values"></a>Values

Os valores para filtragem de spam são:
  
|**Nível de spam**|**Valor**|
|:-----|:-----|
|Nenhum  <br/> |0xFFFFFFFF  <br/> |
|Baixa  <br/> |0x00000006  <br/> |
|Médio  <br/> |0x00000005  <br/> |
|Alta  <br/> |0x00000003  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências relacionados especificações de protocolo do Microsoft Exchange Server e as definições de conjunto de propriedades.
    
[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)
  
> Permite a manipulação das listas de permitir/bloquear e a determinação das mensagens de lixo eletrônico.
    
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

