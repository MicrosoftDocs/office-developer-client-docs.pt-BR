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
ms.openlocfilehash: 01d4391850067d00645b5c0248e1bf858c2a9049
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768332"
---
# <a name="pidlidcategories-canonical-property"></a>Propriedade canônica PidLidCategories

  
  
**Aplica-se a**: Outlook 
  
Especifica uma lista de categorias para um item.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |dispidCategories  <br/> |
|Propriedade definida:  <br/> |PS_PUBLIC_STRINGS  <br/> |
|ID de longo (LID):  <br/> |0x00002328  <br/> |
|Tipo de dados:  <br/> |PT_MV_UNICODE  <br/> |
|Área:  <br/> |Comuns  <br/> |
   
## <a name="remarks"></a>Comentários

Para gerar um campo de cabeçalho de palavras-chave, os clientes devem definir o valor dessa propriedade para os valores desejados. Esta propriedade tem várias cadeias de caracteres; cada categoria deve ser mapeada para uma única palavra-chave.
  
Escritores de Multipurpose Internet Mail Extensions (MIME) devem copiar cada valor sub-recurso dessa propriedade para uma palavra-chave separada no campo de cabeçalho de palavras-chave, com uma vírgula (U + 002 C) e (U + 0020) de espaço separando cada palavra-chave. Os autores MIME poderão perder essa propriedade em vez de copiá-lo para o campo de cabeçalho de palavras-chave, para evitar conflitos entre conjuntos diferentes das categorias em organizações diferentes.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece a definição de propriedade do conjunto e referências para relacionados especificações de protocolo do Exchange Server.
    
[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Converte de convenções de email padrão da Internet para os objetos de mensagem.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

