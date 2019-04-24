---
title: Propriedade canônica PidTagSearchAttachments
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 534c3881-e12f-f228-7760-788fe2b72ae8
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 95729474db29fe21f808ec5c8f571bec4600db70
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336320"
---
# <a name="pidtagsearchattachments-canonical-property"></a>Propriedade canônica PidTagSearchAttachments

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém uma cadeia de caracteres Unicode que está sendo consultada no conteúdo do anexo no repositório.
  
## 

|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_SEARCH_ATTACHMENTS_W  <br/> |
|Identificador:  <br/> |0x0EA5  <br/> |
|Tipo de propriedade:  <br/> |PT_UNICODE  <br/> |
|Área:  <br/> |Pesquisa  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

> [!NOTE]
> Essa marca de restrição MAPI, usada quando você está pesquisando o conteúdo do anexo, não pode ser definida no arquivo de cabeçalho baixado que você tem atualmente. Você pode adicioná-lo ao seu código usando o seguinte valor: >`#define PR_SEARCH_ATTACHMENTS_W PROP_TAG(PT_UNICODE, 0x0EA5)`
  
### <a name="protocol-specifications"></a>Especificações do protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências para as especificações de protocolo do Microsoft Exchange Server relacionadas.
    
[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)
  
> Especifica as propriedades e operações para manipular uma configuração de lista de pastas de pesquisa.
    
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

