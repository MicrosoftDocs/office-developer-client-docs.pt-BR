---
title: Propriedade canônica PidTagAdditionalRenEntryIds
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAdditionalRenEntryIds
api_type:
- HeaderDef
ms.assetid: 8c6e7ca2-1824-4cca-bf69-3c1ea52727de
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: e63d661ab8c7e410d6a0dd786819cc189813017e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768914"
---
# <a name="pidtagadditionalrenentryids-canonical-property"></a>Propriedade canônica PidTagAdditionalRenEntryIds

  
  
**Aplica-se a**: Outlook 
  
Contém a entrada de identificações de determinadas pastas especiais. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_ADDITIONAL_REN_ENTRYIDS  <br/> |
|Identificador:  <br/> |0x36D8  <br/> |
|Tipo de dados:  <br/> |PT_MV_BINARY  <br/> |
|Área:  <br/> |Aplicativo do Outlook  <br/> |
   
## <a name="remarks"></a>Comentários

As cinco primeiras entradas dessa propriedade de valores múltiplos se aplicam às seguintes pastas especiais, se elas existirem no repositório de:
  
0 - pasta conflitos
  
1 - pasta de problemas de sync
  
2 - pasta falhas locais
  
3 - pasta de falhas de servidor
  
4 - pasta Lixo eletrônico
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a relacionados especificações de protocolo do Exchange Server.
    
[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)
  
> Especifica as propriedades e operações para a criação e a localização de pastas especiais em uma caixa de correio.
    
[[MS-OXPHISH]](http://msdn.microsoft.com/library/ed49ab26-ba13-4d4c-8a94-98d4ceecd4b7%28Office.15%29.aspx)
  
> Identifica e marca mensagens de email que foram projetadas para fazer com que os destinatários a divulgação de informações confidenciais (por exemplo, senhas e outras informações pessoais) para uma fonte não confiável.
    
[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)
  
> Permite a manipulação das listas de permitir/bloquear e a determinação das mensagens de lixo eletrônico.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapitags.h
  
> Contém definições das propriedades listadas como propriedades associadas.
    
Mapidefs.h
  
> Fornece definições de tipo de dados.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)


[Sobre a API de armazenamento](http://msdn.microsoft.com/en-us/library/aa192884.aspx)

