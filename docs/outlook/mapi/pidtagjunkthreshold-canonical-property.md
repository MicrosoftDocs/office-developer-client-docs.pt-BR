---
title: Propriedade canônica PidTagJunkThreshold
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagJunkThreshold
api_type:
- HeaderDef
ms.assetid: 8067e2b5-02df-4b96-8f66-509f5a48c8aa
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 078dfcc7c24870cf95a2a4b2385c34fbeb64fac0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326849"
---
# <a name="pidtagjunkthreshold-canonical-property"></a>Propriedade canônica PidTagJunkThreshold

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Indica o quão agressivamente as mensagens de entrada devem ser enviadas para a pasta lixo eletrônico.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_JUNK_THRESHOLD  <br/> |
|Identificador:  <br/> |0x6101  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Spam  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade corresponde à configuração de filtro alto/baixo/nenhuma. Um valor de "0xFFFFFFFF" indica que a filtragem de spam não deve ser aplicada, mas listas de bloqueios ainda devem ser aplicadas. Um valor de "0x80000000" indica que todos os emails são spam, exceto as mensagens dos remetentes na lista de remetentes confiáveis ou enviados para os destinatários na lista de destinatários confiáveis. Os valores para isso são os seguintes:
  
|**Valor**|**Descrição**|
|:-----|:-----|
|0xFFFFFFFF  <br/> |Sem filtragem de spam  <br/> |
|0x00000006  <br/> |Filtragem de spam baixa  <br/> |
|0x00000003  <br/> |Filtragem alta de spam  <br/> |
|0x80000000  <br/> |Somente listas confiáveis  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações do protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências às especificações relacionadas do protocolo do Exchange Server.
    
[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)
  
> Permite a manipulação de listas de permissões/bloqueios e a determinação de mensagens de lixo eletrônico.
    
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

