---
title: Abrir um contêiner de catálogo de endereços
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 89383b27-618c-4ccb-9e16-f66235c98bfe
description: 'Última modificação: 08 de novembro de 2011'
ms.openlocfilehash: 97fa9f9750174c112c431c62f6171f674856fa86
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436738"
---
# <a name="opening-an-address-book-container"></a>Abrir um contêiner de catálogo de endereços

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Após abrir o catálogo de endereços integrado MAPI, abra um ou mais contêineres do catálogo de endereços para acessar os destinatários dentro deles.
  
Para abrir o contêiner de nível superior do catálogo de endereços, chame [IAddrBook:: OpenEntry](iaddrbook-openentry.md) com um identificador de entrada nulo. 
  
Os contêineres do catálogo de endereços podem ser implementados com acesso somente leitura ou leitura/gravação. Contêineres somente leitura são usados apenas para navegação. Contêineres de leitura/gravação podem ser modificados, permitindo que os clientes criem novas entradas e excluam e modifiquem entradas existentes. Todos os contêineres do catálogo de endereços pessoal (PAB) são implementados como contêineres de leitura/gravação. 
  
Para abrir qualquer contêiner de nível inferior, chame **OpenEntry** e especifique o identificador de entrada do contêiner a ser aberto. 
  
## <a name="open-the-container-designated-as-the-pab"></a>Abra o contêiner designado como o PAB
  
1. Chame [IAddrBook:: GetPAB](iaddrbook-getpab.md) para recuperar o identificador de entrada do PAB. 
    
2. Passe este identificador de entrada para [IAddrBook:: OpenEntry](iaddrbook-openentry.md).
    
## <a name="open-a-container-that-is-not-the-pab"></a>Abrir um contêiner que não seja o PAB
  
1. Chame [IAddrBook:: OpenEntry](iaddrbook-openentry.md) com um identificador de entrada nulo para abrir o contêiner raiz do catálogo de endereços. 
    
2. Chame o método [IMAPIContainer::](imapicontainer-gethierarchytable.md) GetHierarchyTable do contêiner raiz para recuperar sua tabela de hierarquia — uma lista de todos os contêineres de nível superior no catálogo de endereços. 
    
3. Se o contêiner a ser aberto for de um tipo específico:
    
   - Crie uma estrutura **SPropertyRestriction** com **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) para a marca de propriedade, o tipo de contêiner para o valor da propriedade e RELOP_EQ para a relação. **PR_DISPLAY_TYPE** pode ser definido como muitos valores, entre eles: 
    
   - DT_GLOBAL para limitar a tabela de hierarquia a contêineres que pertencem à lista de endereços global.
    
   - DT_LOCAL para limitar a tabela a contêineres pertencentes a um catálogo de endereços local.
    
   - DT_MODIFIABLE para limitar a tabela a contêineres que podem ser modificados.
    
   - Criar uma estrutura [SPropTagArray](sproptagarray.md) que inclui o **PR_ENTRYID**, o **PR_DISPLAY_TYPE**e qualquer outra coluna de interesse. 
    
   - Chame [HrQueryAllRows](hrqueryallrows.md), passando a restrição de propriedade e a matriz de marca de propriedade. **HrQueryAllRows** retornará zero ou mais linhas, uma linha para cada contêiner que pertence ao tipo especificado. Esteja preparado para lidar com o retorno de qualquer número de linhas. 
    
   - Chame **IAddrBook:: OpenEntry** com o identificador de entrada da coluna **PR_ENTRYID** da linha que representa o contêiner de interesse. 
    
4. Se o contêiner a ser aberto pertencer a um provedor de catálogo de endereços específico:
    
   - Crie uma estrutura [SPropertyRestriction](spropertyrestriction.md) com **PR_AB_PROVIDERS** ([PidTagAbProviders](pidtagabproviders-canonical-property.md)) para a marca de propriedade, um valor específico do provedor para o valor da propriedade e RELOP_EQ para a relação. Normalmente, o valor específico do provedor é um identificador global exclusivo ou um GUID. Você encontrará esse valor publicado em um dos arquivos de cabeçalho do provedor de catálogo de endereços. 
    
   - Crie uma estrutura [SPropTagArray](sproptagarray.md) que inclui o **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), o **PR_AB_PROVIDERS**e qualquer outra coluna de interesse. 
    
   - Chame [HrQueryAllRows](hrqueryallrows.md), passando a restrição de propriedade e a matriz de marca de propriedade. **HrQueryAllRows** retornará zero linhas se o provedor de catálogo de endereços especificado não estiver no perfil. Pode retornar uma ou mais linhas para os contêiners de nível superior do provedor, dependendo de como o provedor é organizado. 
    
   - Chame [IAddrBook:: OpenEntry](iaddrbook-openentry.md) com o identificador de entrada da coluna **PR_ENTRYID** da linha que representa o contêiner de interesse. Se o contêiner em que você está interessado não for um contêiner de nível superior, encontre o contêiner de nível superior e atravesse a hierarquia. 
    

