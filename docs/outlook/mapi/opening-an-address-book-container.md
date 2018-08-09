---
title: Abrindo um contêiner de catálogo de endereços
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 89383b27-618c-4ccb-9e16-f66235c98bfe
description: 'Modificado pela última vez: 08 de novembro de 2011'
ms.openlocfilehash: 28f60154524065bd2c818e2e4b7db37ca33276b4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768182"
---
# <a name="opening-an-address-book-container"></a>Abrindo um contêiner de catálogo de endereços

**Aplica-se a**: Outlook 
  
Após a abertura de MAPI integrado catálogo de endereços, abra um ou mais contêineres de catálogo de endereços para acessar os destinatários dentro deles.
  
Para abrir o contêiner de nível superior do catálogo de endereços, chame [IAddrBook::OpenEntry](iaddrbook-openentry.md) com um identificador de entrada NULL. 
  
Contêineres de catálogo de endereços podem ser implementados com somente leitura ou acesso de leitura/gravação. Somente leitura contêineres são usadas somente para pesquisa. Leitura/gravação contêineres podem ser modificados, permitindo que os clientes criar novas entradas e excluir e modificar entradas existentes. Todos os contêineres de catálogo (PAB) particular de endereços são implementados como contêineres de leitura/gravação. 
  
Para abrir qualquer contêiner de nível inferior, chame **OpenEntry** e especifique o identificador de entrada do contêiner ao ser aberto. 
  
## <a name="open-the-container-designated-as-the-pab"></a>Abra o recipiente designado como o PAB
  
1. Chame [IAddrBook::GetPAB](iaddrbook-getpab.md) para recuperar o identificador de entrada do PAB. 
    
2. Passe esse identificador de entrada para [IAddrBook::OpenEntry](iaddrbook-openentry.md).
    
## <a name="open-a-container-that-is-not-the-pab"></a>Abra um contêiner que não seja o PAB
  
1. Chame [IAddrBook::OpenEntry](iaddrbook-openentry.md) com um identificador de entrada NULL para abrir o contêiner de raiz do catálogo de endereços. 
    
2. Chamar o método de [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) do contêiner raiz para recuperar sua tabela de hierarquia — uma lista de todos os contêineres de nível superior no catálogo de endereços. 
    
3. Se o contêiner deve ser aberto for de um tipo específico:
    
   - Crie uma estrutura de **SPropertyRestriction** com **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) para a marca de propriedade, o tipo do recipiente para o valor da propriedade e RELOP_EQ para a relação. **PR_DISPLAY_TYPE** pode ser definido como muitos valores, entre eles: 
    
   - DT_GLOBAL para limitar a tabela de hierarquia aos contêineres que pertencem a lista de endereços global.
    
   - DT_LOCAL para limitar a tabela de contêineres que pertencem a um catálogo de endereços locais.
    
   - DT_MODIFIABLE para limitar a tabela de contêineres que podem ser modificados.
    
   - Crie uma estrutura de [SPropTagArray](sproptagarray.md) que inclui **PR_ENTRYID**, **PR_DISPLAY_TYPE**e quaisquer outras colunas de interesse. 
    
   - Chame [HrQueryAllRows](hrqueryallrows.md), passando sua matriz de marca de propriedade e a restrição de propriedade. **HrQueryAllRows** retornará zero ou mais linhas, de uma linha para cada contêiner que pertence ao tipo especificado. Esteja preparado para lidar com o retorno de qualquer número de linhas. 
    
   - Chame **IAddrBook::OpenEntry** com o identificador de entrada da coluna **PR_ENTRYID** da linha que representa o contêiner de interesse. 
    
4. Se o contêiner deve ser aberto pertencer a um provedor de catálogo de endereço específica:
    
   - Crie uma estrutura de [SPropertyRestriction](spropertyrestriction.md) com **PR_AB_PROVIDERS** ([PidTagAbProviders](pidtagabproviders-canonical-property.md)) para a marca de propriedade, um valor específico do provedor para o valor da propriedade e RELOP_EQ para a relação. Normalmente, o valor de específico do provedor é um identificador globalmente exclusivo ou um GUID. Você encontrará esse valor publicado em um dos arquivos de cabeçalho do provedor de catálogo de endereços. 
    
   - Crie uma estrutura de [SPropTagArray](sproptagarray.md) que inclui **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_AB_PROVIDERS**e quaisquer outras colunas de interesse. 
    
   - Chame [HrQueryAllRows](hrqueryallrows.md), passando sua matriz de marca de propriedade e a restrição de propriedade. **HrQueryAllRows** retornará zero linhas se o provedor de catálogo de endereço especificado não estiver no perfil. Ele pode retornar uma ou mais linhas para contêineres de nível superior do provedor, dependendo de como o provedor é organizado. 
    
   - Chame [IAddrBook::OpenEntry](iaddrbook-openentry.md) com o identificador de entrada da coluna **PR_ENTRYID** da linha que representa o contêiner de interesse. Se o contêiner que você está interessado não for um contêiner de nível superior, localize o contêiner de nível superior e percorrer a hierarquia. 
    

