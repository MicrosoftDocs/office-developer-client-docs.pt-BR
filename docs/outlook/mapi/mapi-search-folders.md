---
title: Pastas de pesquisa MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 36c14d91-77f7-43a3-8d87-d50bcc21fad7
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: e74767f4b3a19442beac5f9c9ac375286bb47c81
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767935"
---
# <a name="mapi-search-folders"></a>Pastas de pesquisa MAPI

  
  
**Aplica-se a**: Outlook 
  
Uma pasta de resultados de pesquisa contém links para as mensagens nas pastas genéricas em vez das mensagens reais. Clientes crie uma pasta de resultados de pesquisa chamando o método [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) com FOLDER_SEARCH como o parâmetro _ulFolderType_ . Clientes preencher uma pasta de resultados de pesquisa, configurando e a aplicação de critérios de pesquisa — regras que filtram mensagens com características específicas. Critérios de pesquisa são configurados com o método [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) . Clientes construa uma ou mais estruturas [SRestriction](srestriction.md) para representar os critérios de pesquisa será aplicado e passá-las para **definir SetSearchCriteria**. **Definir SetSearchCriteria** também especifica uma lista de pastas que indicam o domínio de pesquisa e um conjunto de sinalizadores que controlam como a pesquisa é realizada. 
  
 **Definir SetSearchCriteria** identifica as mensagens que correspondem a restrição especificada. As mensagens selecionadas (aqueles que satisfazem os critérios) são exibidas como links na pasta resultados de pesquisa. Quando o cliente chama o método [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) para acessar a tabela de conteúdo da pasta resultados de pesquisa, as mensagens selecionadas são exibidas na tabela. Tabelas de conteúdo para pastas de resultados de pesquisa contêm as mesmas colunas como tabelas de conteúdo para pastas genéricas. No entanto, para pastas de resultados da pesquisa, a propriedade **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) Especifica o identificador de entrada da pasta em que a mensagem vinculada reside. Pastas de resultados de pesquisa não são consideradas pastas pai.
  
Pastas de resultados de pesquisa tem os seguintes limites:
  
- A única maneira que o conteúdo de uma pasta de resultados de pesquisa pode ser modificado é por meio de uma chamada para **definir SetSearchCriteria**. Para obter mais informações sobre a implementação do **definir SetSearchCriteria**, consulte o artigo [260322: como para pastas de pesquisa com o método definir SetSearchCriteria](http://go.microsoft.com/fwlink/?LinkId=123603).
    
- As mensagens não podem ser movidas ou copiadas em pastas de resultados de pesquisa.
    
- Pastas de resultados de pesquisa não podem conter subpastas. 
    
- Os clientes não podem fazer uma pasta de resultados de pesquisa o assunto de uma pesquisa.
    
No entanto, é possível, para modificar as propriedades de uma pasta de resultados de pesquisa e usá-lo para excluir uma mensagem. Quando uma mensagem é excluída de uma pasta de resultados de pesquisa, ser realmente excluído da pasta real. No entanto, excluindo a própria pasta de resultados de pesquisa tem nenhum impacto sobre as mensagens dentro; eles permanecem em suas pastas genéricas.
  
## <a name="see-also"></a>Confira também



[Pastas MAPI](mapi-folders.md)

