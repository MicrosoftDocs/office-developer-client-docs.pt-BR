---
title: Propriedade canônica PidLidSpamOriginalFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSpamOriginalFolder
api_type:
- COM
ms.assetid: 45846fe3-7ab3-4019-98bb-fe615889c31c
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 561008782e7c1ffb8bc71cf4e3bc17befe69bbca
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331553"
---
# <a name="pidlidspamoriginalfolder-canonical-property"></a>Propriedade canônica PidLidSpamOriginalFolder

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Indica a pasta em que a mensagem estava antes de ser filtrada para a pasta lixo eletrônico.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |dispidSpamOriginalFolder  <br/> |
|Conjunto de propriedades:  <br/> |PSETID_Common  <br/> |
|Long ID (LID):  <br/> |0x0000859C  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Spam  <br/> |
   
## <a name="remarks"></a>Comentários

O valor dessa propriedade é a **EntryID** da pasta que continha a mensagem antes de ser movida. Essa propriedade deve ser definida quando uma mensagem é marcada como spam. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações do protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece definições e referências de conjuntos de propriedades para especificações de protocolo do Exchange Server relacionadas.
    
[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)
  
> Permite a manipulação de listas de permissões/bloqueios e a determinação de mensagens de lixo eletrônico.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs. h
  
> Fornece definições de tipo de dados.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

