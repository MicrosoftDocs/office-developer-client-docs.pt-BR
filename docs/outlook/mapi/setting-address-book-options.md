---
title: Configurar opções de Catálogo de Endereços
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9bd31233-fc8d-4e0a-9f1b-218c5ecb6d1b
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: c64f84da6bece809176bf67985b6f55ce92414a2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770381"
---
# <a name="setting-address-book-options"></a>Configurar opções de Catálogo de Endereços

  
  
**Aplica-se a**: Outlook 
  
Você pode definir três propriedades que descrevem as opções para usar o catálogo de endereços:
  
- **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md))
    
    A propriedade **PR_AB_SEARCH_PATH** é usada pelo [IAddrBook::ResolveName](iaddrbook-resolvename.md) para determinar os contêineres estar envolvidos na resolução de nome e a ordem que devem ser envolvidos. Para cada contêiner no **PR_AB_SEARCH_PATH**, **IAddrBook::ResolveName** chama seu método de [IABContainer:: ResolveNames](iabcontainer-resolvenames.md) . Contêineres no início do **PR_AB_SEARCH_PATH** são pesquisados antes de contêineres no final da **PR_AB_SEARCH_PATH**. 
    
    A ordem de pesquisa no **PR_AB_SEARCH_PATH** é especificada usando uma estrutura [SRowSet](srowset.md) , a mesma estrutura que é usada para representar as linhas em uma tabela. Você pode exibir o caminho de pesquisa atual chamando o método [IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md) e alterá-lo chamando o método [IAddrBook::SetSearchPath](iaddrbook-setsearchpath.md) . 
    
- **PR_AB_DEFAULT_DIR** ([PidTagAbDefaultDir](pidtagabdefaultdir-canonical-property.md))
    
    A propriedade **PR_AB_DEFAULT_DIR** é o identificador de entrada do contêiner de catálogo de endereços a ser exibido inicialmente quando o catálogo de endereços é exibido. A configuração padrão do diretório permanece em vigor até você alterá-lo chamando o método [IAddrBook::SetDefaultDir](iaddrbook-setdefaultdir.md) . Você pode exibir o diretório padrão chamando o método [IAddrBook::GetDefaultDir](iaddrbook-getdefaultdir.md) . 
    
- **PR_AB_DEFAULT_PAB** ([PidTagAbDefaultPab](pidtagabdefaultpab-canonical-property.md))
    
Essas três propriedades são especiais porque você não pode trabalhar com eles com os métodos **IMAPIProp** padrão. Em vez disso, você deve usar os métodos **IAddrBook** . Porque nenhuma dessas propriedades pode ser alterada com **IMAPIProp::SetProps**, não é necessário chamar **IMAPIProp::SaveChanges** para fazer alterações permanentes. As modificações feitas por meio dos métodos **IAddrBook** entrarão em vigor imediatamente. 
  
## <a name="see-also"></a>Confira também



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

