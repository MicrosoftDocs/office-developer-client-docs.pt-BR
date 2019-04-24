---
title: Definindo opções do catálogo de endereços
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9bd31233-fc8d-4e0a-9f1b-218c5ecb6d1b
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: f72c916e917543b11089f8f5ef1aa4b9552a1b6a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351405"
---
# <a name="setting-address-book-options"></a>Definindo opções do catálogo de endereços

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Você pode definir três propriedades que descrevem as opções de uso do catálogo de endereços:
  
- **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md))
    
    A propriedade **PR_AB_SEARCH_PATH** é usada por [IAddrBook:: ResolveName](iaddrbook-resolvename.md) para determinar os contêineres a serem envolvidos na resolução de nomes e a ordem em que devem ser envolvidos. Para cada contêiner em **PR_AB_SEARCH_PATH**, **IAddrBook:: ResolveName** chama seu método [IABContainer:: ResolveNames](iabcontainer-resolvenames.md) . Os contêineres no início de **PR_AB_SEARCH_PATH** são pesquisados antes dos contêineres no final de **PR_AB_SEARCH_PATH**. 
    
    A ordem de pesquisa no **PR_AB_SEARCH_PATH** é especificada usando uma estrutura [SRowSet](srowset.md) , a mesma estrutura que é usada para representar linhas em uma tabela. Você pode exibir o caminho de pesquisa atual chamando o método [IAddrBook:: GetSearchPath](iaddrbook-getsearchpath.md) e alterá-lo chamando o método [IAddrBook:: SetSearchPath](iaddrbook-setsearchpath.md) . 
    
- **PR_AB_DEFAULT_DIR** ([PidTagAbDefaultDir](pidtagabdefaultdir-canonical-property.md))
    
    A propriedade **PR_AB_DEFAULT_DIR** é o identificador de entrada do contêiner de catálogo de endereços a ser exibido inicialmente quando o catálogo de endereços é exibido. A configuração de diretório padrão permanece em vigor até que você a altere chamando o método [IAddrBook:: SetDefaultDir](iaddrbook-setdefaultdir.md) . Você pode exibir o diretório padrão chamando o método [IAddrBook:: GetDefaultDir](iaddrbook-getdefaultdir.md) . 
    
- **PR_AB_DEFAULT_PAB** ([PidTagAbDefaultPab](pidtagabdefaultpab-canonical-property.md))
    
Essas três propriedades são especiais porque você não pode trabalhar com elas usando os métodos **IMAPIProp** padrão. Em vez disso, você deve usar os métodos **IAddrBook** . Como nenhuma dessas propriedades pode ser alterada com **IMAPIProp::** o SetProps, não é necessário chamar **IMAPIProp:: SaveChanges** para tornar as alterações permanentes. As modificações feitas por meio dos métodos **IAddrBook** entram em vigor imediatamente. 
  
## <a name="see-also"></a>Confira também



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

