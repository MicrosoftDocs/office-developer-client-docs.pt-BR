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
ms.openlocfilehash: d43a0229f232f9437d1746799534c0f2d6fba83f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346309"
---
# <a name="pidtagspamthreshold-canonical-property"></a>Propriedade canônica PidTagSpamThreshold

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Um valor longo que indica o nível de filtragem de spam.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_SPAM_THRESHOLD  <br/> |
|Long ID (LID):  <br/> | 0x041B  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Spam  <br/> |
   
## <a name="values"></a>Values

Os valores para filtragem de spam são os seguinte:
  
|**Nível de spam**|**Valor**|
|:-----|:-----|
|Nenhum  <br/> |0xFFFFFFFF  <br/> |
|Baixo  <br/> |0x00000006  <br/> |
|Médio  <br/> |0x00000005  <br/> |
|Alto  <br/> |0x00000003  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece definições de conjunto de propriedades e referências a especificações de protocolo do Microsoft Exchange Server relacionadas.
    
[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)
  
> Permite a manipulação de listas de bloqueio/autorização e a determinação de mensagens de lixo eletrônico.
    
### <a name="header-files"></a>Arquivos de header

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições de propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapeando nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapeando nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

