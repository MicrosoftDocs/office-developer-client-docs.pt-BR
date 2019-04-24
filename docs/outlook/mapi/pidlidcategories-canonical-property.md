---
title: Propriedade canônica PidLidCategories
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidCategories
api_type:
- COM
ms.assetid: 6ad2aedc-405b-475e-ac76-7ecbbef28f73
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: b2047f04f3f4a8d2b3e58e07a71e7e2463eff9cf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344972"
---
# <a name="pidlidcategories-canonical-property"></a>Propriedade canônica PidLidCategories

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Especifica uma lista de categorias para um item.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |dispidCategories  <br/> |
|Conjunto de propriedades:  <br/> |PS_PUBLIC_STRINGS  <br/> |
|Long ID (LID):  <br/> |0x00002328  <br/> |
|Tipo de dados:  <br/> |PT_MV_UNICODE  <br/> |
|Área:  <br/> |Comum  <br/> |
   
## <a name="remarks"></a>Comentários

Para gerar um campo de cabeçalho keywords, os clientes devem definir o valor dessa propriedade para os valores desejados. Essa propriedade tem várias cadeias de caracteres; cada categoria deve ser mapeada para uma única palavra-chave.
  
Os gravadores de MIME (Multipurpose Internet Mail Extensions) devem copiar cada subvalor dessa propriedade para uma palavra-chave separada no campo de cabeçalho keywords, com uma vírgula (U + 002C) e espaço (U + 0020) separando cada palavra-chave. Os gravadores MIME podem descartar essa propriedade em vez de copiá-la para o campo de cabeçalho keywords, a fim de evitar o conflito entre diferentes conjuntos de categorias em diferentes organizações.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações do protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece definição e referências de conjunto de propriedades para especificações de protocolo do Exchange Server relacionadas.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Converte as convenções de email padrão da Internet em objetos de mensagem.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs. h
  
> Fornece definições de tipo de dados.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

