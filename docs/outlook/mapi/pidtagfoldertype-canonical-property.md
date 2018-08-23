---
title: Propriedade canônica PidTagFolderType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFolderType
api_type:
- HeaderDef
ms.assetid: 2ab4681e-0013-4ba0-ba26-50517bbf3f5b
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 8d6167a7a3c983171f2ff9cb2a54c879a14dca0e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591412"
---
# <a name="pidtagfoldertype-canonical-property"></a>Propriedade canônica PidTagFolderType

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém uma constante que indica o tipo de pasta. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_FOLDER_TYPE  <br/> |
|Identificador:  <br/> |0x3601  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Contêiner MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade pode ter exatamente um dos seguintes valores:
  
FOLDER_GENERIC 
  
> Uma pasta genérica que contém mensagens e outras pastas.
    
FOLDER_ROOT 
  
> A pasta raiz da tabela de hierarquia de pasta, ou seja, uma pasta que não tenha nenhuma pasta pai.
    
FOLDER_SEARCH 
  
> Uma pasta que contém os resultados de uma pesquisa, na forma de links para mensagens que atendam aos critérios de pesquisa.
    
A raiz de um armazenamento de mensagens não deve ser confundida com a raiz da subárvore interpessoais mensagens (IPM) desse repositório. Pasta raiz da loja, o que não tem um pai, é obtida chamando o método [IMsgStore::OpenEntry](imsgstore-openentry.md) com um identificador de entrada nulo. Pasta raiz do subárvore IPM, que tem um pai, é obtida usando-se o valor da propriedade **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) para a chamada **OpenEntry** . 
  
MAPI permite que apenas uma pasta raiz por repositório de mensagem. Essa pasta contém mensagens e outras pastas. Propriedade de **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) da pasta raiz contém o identificador de entrada da pasta.
  
As informações em uma pasta de resultados de pesquisa principalmente são armazenadas em sua tabela de conteúdo, que contém as mesmas colunas como uma tabela de conteúdo típico, bem como duas colunas adicionais que identifica a pasta na qual cada mensagem foi encontrada: **PR_PARENT_DISPLAY** ([ PidTagParentDisplay](pidtagparentdisplay-canonical-property.md)) (exibir o nome, necessário) e essa propriedade (identificador entrada, opcional).
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a relacionados especificações de protocolo do Exchange Server.
    
[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> Trata as operações de pasta.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições das propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

