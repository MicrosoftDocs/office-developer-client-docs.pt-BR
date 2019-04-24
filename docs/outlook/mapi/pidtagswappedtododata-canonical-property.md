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
ms.openlocfilehash: 3ecfa1e89688ae525a28e221424fb4a8194fc217
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359133"
---
# <a name="pidtagswappedtododata-canonical-property"></a>Propriedade canônica PidTagSwappedToDoData

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Mantém um segundo conjunto de valores de propriedade que não afetam o estado sinalizado do objeto Message.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_SWAPPED_TODO_DATA  <br/> |
|Identificador:  <br/> |0x0E2D  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |MAPI não-transmittable  <br/> |
   
## <a name="remarks"></a>Comentários

Atuando como o local de armazenamento de sinalizador secundário se houver suporte para sinalizadores de remetente ou lembretes de remetente, essa estrutura fornecerá um local no qual serão armazenadas todas as propriedades relacionadas ao protocolo de sinalização inFormativo que têm suporte nos sinalizadores de remetente e todos os Propriedades relacionadas ao protocolo de configurações de lembrete que são compatíveis com lembretes de remetente sem expor as informações de sinalizador de remetente ou de lembrete para os destinatários de uma mensagem.
  
Da mesma forma, essa estrutura fornece um local no qual armazenar todas as propriedades relacionadas ao protocolo de sinalização inFormativo que são suportados em sinalizadores de destinatário e propriedades relacionadas ao protocolo de configurações de lembrete que são suportados no destinatário lembretes em uma mensagem enviada anteriormente.
  
Para obter mais informações sobre essa propriedade, consulte [[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx).
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações do protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências às especificações relacionadas do protocolo do Exchange Server.
    
[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Especifica as propriedades e operações relacionadas à sinalização.
    
[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)
  
> Especifica as propriedades e o modelo de interação para email e outros lembretes de objeto.
    
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

