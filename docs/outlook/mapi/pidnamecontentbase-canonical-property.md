---
title: Propriedade canônica PidNameContentBase
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidNameContentBase
api_type:
- COM
ms.assetid: ab197ace-6e7d-4ec5-9f6d-4a63a1eda11c
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 501b54cfb7846a91aec7172cbe1d846c24704923
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331497"
---
# <a name="pidnamecontentbase-canonical-property"></a>Propriedade canônica PidNameContentBase

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém um valor de campo de cabeçalho Content-base de conteúdo de [RFC3282].
  
|||
|:-----|:-----|
|Nomes amigáveis:  <br/> |BodyContentBase  <br/> |
|Conjunto de propriedades:  <br/> |PS_INTERNET_HEADERS  <br/> |
|Nome da propriedade:  <br/> |Conteúdo-base  <br/> |
|Tipo de dados:  <br/> |PT_UNICODE  <br/> |
|Área:  <br/> |Email  <br/> |
   
## <a name="remarks"></a>Comentários

Para definir o valor dessa propriedade, os clientes MIME (Multipurpose Internet Message Extensions) devem gravar o valor desejado em um campo de cabeçalho de base de conteúdo em uma entidade MIME que mapeia para um corpo de mensagem. Os leitores MIME devem copiar o valor de um campo de cabeçalho Content-base em uma entidade MIME para o valor dessa propriedade.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações do protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece definições e referências de conjuntos de propriedades para especificações de protocolo do Exchange Server relacionadas.
    
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

