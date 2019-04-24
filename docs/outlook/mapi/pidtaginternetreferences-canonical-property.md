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
ms.openlocfilehash: 431a212b6e024d695fe2de084080996d8b1054d6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360407"
---
# <a name="pidtaginternetreferences-canonical-property"></a>Propriedade canônica PidTagInternetReferences

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém o valor de um campo de cabeçalho referências de mensagens de MIME (Multipurpose Internet Mail Extensions).
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_INTERNET_REFERENCES, PR_INTERNET_REFERENCES_A, PR_INTERNET_REFERENCES_W  <br/> |
|Identificador:  <br/> |0x1039  <br/> |
|Tipo de dados:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |MIME  <br/> |
   
## <a name="remarks"></a>Comentários

Para gerar um campo de cabeçalho References, os clientes devem definir essas propriedades com o valor desejado. Os gravadores MIME devem copiar o valor dessas propriedades para o campo de cabeçalho References.
  
Para definir o valor dessas propriedades, os clientes MIME devem gravar o valor desejado em um campo de cabeçalho References. Leitores MIME devem copiar o valor do campo de cabeçalho References para essas propriedades. Leitores MIME podem truncar o valor dessas propriedades se ele exceder 64 KB de comprimento.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações do protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências às especificações relacionadas do protocolo do Exchange Server.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Converte as convenções de email padrão da Internet em objetos de mensagem.
    
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

