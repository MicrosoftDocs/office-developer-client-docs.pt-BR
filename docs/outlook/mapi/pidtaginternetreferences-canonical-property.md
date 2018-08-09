---
title: Propriedade canônica PidTagInternetReferences
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagInternetReferences
api_type:
- HeaderDef
ms.assetid: 645fe61d-414a-455e-b034-db3cfd003b9d
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 4558fcdba11aed92eb21972ed62320209ade77ad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769377"
---
# <a name="pidtaginternetreferences-canonical-property"></a>Propriedade canônica PidTagInternetReferences

  
  
**Aplica-se a**: Outlook 
  
Contém o valor do campo de cabeçalho de referências de uma mensagem email extensões MIME (Multipurpose Internet).
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_INTERNET_REFERENCES, PR_INTERNET_REFERENCES_A, PR_INTERNET_REFERENCES_W  <br/> |
|Identificador:  <br/> |0x1039  <br/> |
|Tipo de dados:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |MIME  <br/> |
   
## <a name="remarks"></a>Comentários

Para gerar um campo de cabeçalho de referências, os clientes devem definir essas propriedades para o valor desejado. Os autores MIME devem copiar o valor dessas propriedades no campo de cabeçalho de referências.
  
Para definir o valor dessas propriedades, os clientes MIME devem gravar o valor desejado a um campo de cabeçalho de referências. Leitores MIME devem copiar o valor do campo de cabeçalho de referências a essas propriedades. Leitores MIME podem truncar o valor dessas propriedades se ela exceder 64KB de comprimento.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a relacionados especificações de protocolo do Exchange Server.
    
[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Converte de convenções de email padrão da Internet para os objetos de mensagem.
    
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

