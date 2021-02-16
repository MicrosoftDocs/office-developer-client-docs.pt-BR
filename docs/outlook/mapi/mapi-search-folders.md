---
title: Pastas de Pesquisa MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 36c14d91-77f7-43a3-8d87-d50bcc21fad7
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: c1d7f67458852319587d98831d031b2c3a131871
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357670"
---
# <a name="mapi-search-folders"></a>Pastas de Pesquisa MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Uma pasta de resultados de pesquisa contém links para mensagens em pastas genéricas em vez das mensagens reais. Os clientes criam uma pasta de resultados de pesquisa chamando o método [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) com FOLDER_SEARCH como _o parâmetro ulFolderType._ Os clientes preenchem uma pasta de resultados de pesquisa configurando e aplicando critérios de pesquisa regras que filtram mensagens com características específicas. Os critérios de pesquisa são definidos com o [método IMAPIContainer::SetSearchCriteria.](imapicontainer-setsearchcriteria.md) Os clientes criar uma ou mais estruturas [SRestriction](srestriction.md) para representar os critérios de pesquisa a serem aplicados e passá-las **para SetSearchCriteria**. **SetSearchCriteria** também especifica uma lista de pastas que indicam o domínio de pesquisa e um conjunto de sinalizadores que controlam como a pesquisa é realizada. 
  
 **SetSearchCriteria** identifica as mensagens que corresponderem à restrição especificada. As mensagens selecionadas (aquelas que atendem aos critérios) são exibidas como links na pasta resultados da pesquisa. Quando o cliente chama o método [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) para acessar o índice de conteúdo da pasta de resultados da pesquisa, as mensagens selecionadas são exibidas na tabela. Tabelas de conteúdo para pastas de resultados de pesquisa contêm as mesmas colunas que as tabelas de conteúdo para pastas genéricas. No entanto, para pastas de resultados de pesquisa, a propriedade **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) especifica o identificador de entrada da pasta onde reside a mensagem vinculada. Pastas de resultados de pesquisa não são consideradas pastas pai.
  
As pastas de resultados de pesquisa têm os seguintes limites:
  
- A única maneira que o conteúdo de uma pasta de resultados de pesquisa pode ser modificado é através de uma chamada para **SetSearchCriteria**. Para obter mais informações sobre a implementação de **SetSearchCriteria**, consulte o artigo [260322](https://go.microsoft.com/fwlink/?LinkId=123603)da Base de Dados de Conhecimento: Como pesquisar pastas com o método SetSearchCriteria .
    
- As mensagens não podem ser movidas ou copiadas para pastas de resultados de pesquisa.
    
- Pastas de resultados de pesquisa não podem conter subpastas. 
    
- Os clientes não podem tornar uma pasta de resultados de pesquisa o assunto de uma pesquisa.
    
No entanto, é possível modificar as propriedades de uma pasta de resultados de pesquisa e usá-la para excluir uma mensagem. Quando uma mensagem é excluída de uma pasta de resultados de pesquisa, ela é realmente excluída da pasta real. No entanto, excluir a própria pasta de resultados de pesquisa não afeta as mensagens internas; eles permanecem em suas pastas genéricas.
  
## <a name="see-also"></a>Confira também



[Pastas MAPI](mapi-folders.md)

