---
title: Propriedade canônica PidTagSwappedToDoData
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSwappedToDoData
api_type:
- COM
ms.assetid: d2a82fc8-de5d-4819-906e-b8314fd06ea0
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 8086bc3ea35fdbb4e0f7758b7931e305259a3a9e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578665"
---
# <a name="pidtagswappedtododata-canonical-property"></a>Propriedade canônica PidTagSwappedToDoData

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Mantém um segundo conjunto de valores de propriedade que não afetam o estado sinalizado do objeto de mensagem.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_SWAPPED_TODO_DATA  <br/> |
|Identificador:  <br/> |0x0E2D  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |MAPI não transmittable  <br/> |
   
## <a name="remarks"></a>Comentários

Atuando como o local de armazenamento de sinalizador secundário, se houver suporte para sinalizadores de remetente ou lembretes do remetente, esta estrutura oferece um local na qual armazenar todas as propriedades relacionadas ao protocolo de sinalização informativos suportados no sinalizadores de remetente e todos propriedades relacionadas ao protocolo lembrete configurações que são compatíveis com os lembretes de remetente sem expor o sinalizador de remetente ou informações de lembrete do remetente para os destinatários de uma mensagem.
  
Da mesma forma, esta estrutura oferece um local na qual armazenar todas as propriedades relacionadas ao protocolo de sinalização informativos suportados no destinatários sinalizadores e propriedades relacionadas ao protocolo lembrete configurações que são compatíveis com o destinatário lembretes em uma mensagem enviada anteriormente.
  
Para obter mais informações sobre essa propriedade, consulte [[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx).
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a relacionados especificações de protocolo do Exchange Server.
    
[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Especifica as propriedades e operações relacionadas a sinalização.
    
[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)
  
> Especifica as propriedades e o modelo de interação para email e lembretes de outro objeto.
    
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

