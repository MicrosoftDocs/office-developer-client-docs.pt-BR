---
title: Pastas de pesquisa MAPI
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
# <a name="mapi-search-folders"></a>Pastas de pesquisa MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Uma pasta de resultados de pesquisa contém links para mensagens em pastas genéricas, em vez de mensagens reais. Os clientes criam uma pasta de resultados de pesquisa chamando o método [IMAPIFolder:: CreateFolder](imapifolder-createfolder.md) com FOLDER_SEARCH como o parâmetro _ulFolderType_ . Os clientes preenchem uma pasta de resultados de pesquisa Configurando e aplicando critérios de pesquisa — regras que filtram mensagens com características específicas. Os critérios de pesquisa são configurados com o método [IMAPIContainer:: SetSearchCriteria](imapicontainer-setsearchcriteria.md) . Os clientes criam uma ou mais estruturas [SRestriction](srestriction.md) para representar os critérios de pesquisa a serem aplicados e passá-los para o **SetSearchCriteria**. **SetSearchCriteria** também especifica uma lista de pastas que indicam o domínio de pesquisa e um conjunto de sinalizadores que controlam como a pesquisa é realizada. 
  
 **SetSearchCriteria** identifica as mensagens que correspondem à restrição especificada. As mensagens selecionadas (as que satisfazem os critérios) são exibidas como links na pasta Search-Results. Quando o cliente chama o método [IMAPIContainer::](imapicontainer-getcontentstable.md) getcontenttable para acessar a tabela de conteúdo da pasta de resultados de pesquisa, as mensagens selecionadas são exibidas na tabela. As tabelas de conteúdo das pastas de resultados de pesquisa contêm as mesmas colunas que as tabelas de conteúdo para pastas genéricas. No enTanto, para pastas de resultados de pesquisa, a propriedade **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) especifica o identificador de entrada da pasta onde a mensagem vinculada reside. As pastas de resultados de pesquisa não são consideradas pastas pai.
  
As pastas de resultados de pesquisa têm os seguintes limites:
  
- A única maneira de que o conteúdo de uma pasta de resultados de pesquisa pode ser modificado é por meio de uma chamada a **SetSearchCriteria**. Para obter mais informações sobre a implementação do **SetSearchCriteria**, consulte o artigo 260322 da base de dados de conhecimento [: como pesquisar pastas com o método SetSearchCriteria](https://go.microsoft.com/fwlink/?LinkId=123603).
    
- As mensagens não podem ser movidas ou copiadas para pastas de resultados de pesquisa.
    
- Search-Result Folders não podem conter subpastas. 
    
- Os clientes não podem criar uma pasta de resultados de pesquisa o assunto de uma pesquisa.
    
No entanto, é possível modificar as propriedades de uma pasta de resultados de pesquisa e usá-la para excluir uma mensagem. Quando uma mensagem é excluída de uma pasta de resultados de pesquisa, ela é realmente excluída da pasta real. No enTanto, excluir a pasta de resultados de pesquisa em si não tem impacto nas mensagens de dentro; Eles permanecem em suas pastas genéricas.
  
## <a name="see-also"></a>Confira também



[Pastas MAPI](mapi-folders.md)

