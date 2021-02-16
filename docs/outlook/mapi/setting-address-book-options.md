---
title: Definindo opções do address book
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9bd31233-fc8d-4e0a-9f1b-218c5ecb6d1b
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: f72c916e917543b11089f8f5ef1aa4b9552a1b6a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417340"
---
# <a name="setting-address-book-options"></a>Definindo opções do address book

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Você pode definir três propriedades que descrevem opções para usar o address book:
  
- **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md))
    
    A **PR_AB_SEARCH_PATH** propriedade é usada por [IAddrBook::ResolveName](iaddrbook-resolvename.md) para determinar os contêineres a serem envolvidos na resolução de nomes e na ordem em que eles devem estar envolvidos. Para cada contêiner em **PR_AB_SEARCH_PATH**, **IAddrBook::ResolveName** chama seu [método IABContainer::ResolveNames.](iabcontainer-resolvenames.md) Contêineres no início do **PR_AB_SEARCH_PATH** são pesquisados antes de contêineres no final do **PR_AB_SEARCH_PATH**. 
    
    A ordem de pesquisa **PR_AB_SEARCH_PATH** é especificada usando uma estrutura [SRowSet,](srowset.md) a mesma estrutura usada para representar linhas em uma tabela. Você pode exibir o caminho de pesquisa atual chamando o método [IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md) e alterá-lo chamando o método [IAddrBook::SetSearchPath.](iaddrbook-setsearchpath.md) 
    
- **PR_AB_DEFAULT_DIR** ([PidTagAbDefaultDir](pidtagabdefaultdir-canonical-property.md))
    
    A **PR_AB_DEFAULT_DIR** é o identificador de entrada do contêiner do livro de endereços a ser exibido inicialmente quando o livro de endereços é exibido. A configuração de diretório padrão permanece em vigor até você alterá-la chamando o [método IAddrBook::SetDefaultDir.](iaddrbook-setdefaultdir.md) Você pode exibir o diretório padrão chamando o [método IAddrBook::GetDefaultDir.](iaddrbook-getdefaultdir.md) 
    
- **PR_AB_DEFAULT_PAB** ([PidTagAbDefaultPab](pidtagabdefaultpab-canonical-property.md))
    
Essas três propriedades são especiais porque você não pode trabalhar com elas usando os métodos **IMAPIProp** padrão. Em vez disso, você deve usar **os métodos IAddrBook.** Como nenhuma dessas propriedades pode ser alterada com **IMAPIProp::SetProps,** não há necessidade de chamar **IMAPIProp::SaveChanges** para tornar as alterações permanentes. As modificações feitas por meio **dos métodos IAddrBook** tem efeito imediato. 
  
## <a name="see-also"></a>Confira também



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

