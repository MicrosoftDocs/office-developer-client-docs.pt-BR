---
title: IMAPIContainerSetSearchCriteria
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIContainer.SetSearchCriteria
api_type:
- COM
ms.assetid: b5eb1841-e450-4024-aeaa-3b5a492ddb99
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 93578300e2520dda4a9621b05ac6a79c54eca2ef
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766954"
---
# <a name="imapicontainersetsearchcriteria"></a>IMAPIContainer::SetSearchCriteria

  
  
**Aplica-se a**: Outlook 
  
Estabelece os critérios de pesquisa para o contêiner.
  
```cpp
HRESULT SetSearchCriteria(
  LPSRestriction lpRestriction,
  LPENTRYLIST lpContainerList,
  ULONG ulSearchFlags
);
```

## <a name="parameters"></a>Par�metros

 _lpRestriction_
  
> [in] Um ponteiro para uma estrutura [SRestriction](srestriction.md) que define os critérios de pesquisa. Se NULL é passada no parâmetro _lpRestriction_ , os critérios de pesquisa que foram usados mais recentemente para este contêiner são usados novamente. NULL não deve ser passado no _lpRestriction_ para a pesquisa primeira em um contêiner. 
    
 _lpContainerList_
  
> [in] Um ponteiro para uma matriz de identificadores de entrada que representam os contêineres a serem incluídos na pesquisa. Se um cliente transmite NULL no parâmetro _lpContainerList_ , os identificadores de entrada usados mais recentemente para este contêiner de pesquisa são usados para a nova pesquisa. Um cliente não deve passar NULL no _lpContainerList_ para a pesquisa primeira em um contêiner. 
    
 _ulSearchFlags_
  
> [in] Uma bitmask dos sinalizadores que controlam como a pesquisa é realizada. Sinalizadores a seguir podem ser definidos:
    
BACKGROUND_SEARCH 
  
> A pesquisa deve ser executado com prioridade normal em relação a outras pesquisas. Esse sinalizador não pode ser definida simultaneamente como o sinalizador FOREGROUND_SEARCH.
    
FOREGROUND_SEARCH 
  
> A pesquisa deve ser executado em alta prioridade em relação a outras pesquisas. Esse sinalizador não pode ser definida simultaneamente como o sinalizador BACKGROUND_SEARCH.
    
NON_CONTENT_INDEXED_SEARCH
  
> A pesquisa não deve usar a indexação de conteúdo para encontrar as entradas correspondentes. Esse sinalizador só é válida para repositórios do Exchange.
    
RECURSIVE_SEARCH 
  
> A pesquisa deve incluir os contêineres especificados no parâmetro _lpContainerList_ e todos os seus contêineres filho. Esse sinalizador não pode ser definida simultaneamente como o sinalizador SHALLOW_SEARCH. 
    
RESTART_SEARCH 
  
> A pesquisa deve ser iniciada se esta for a primeira chamada para **definir SetSearchCriteria**ou reiniciada se a pesquisa está inativa. Esse sinalizador não pode ser definida simultaneamente como o sinalizador STOP_SEARCH.
    
SHALLOW_SEARCH 
  
> A pesquisa deve parecer apenas nos contêineres especificados no parâmetro _lpContainerList_ para entradas correspondentes. Esse sinalizador não pode ser definida simultaneamente como o sinalizador RECURSIVE_SEARCH. 
    
STOP_SEARCH 
  
> A pesquisa deve ser interrompida. Esse sinalizador não pode ser definida simultaneamente como o sinalizador RESTART_SEARCH.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> Os critérios de pesquisa foi definida com êxito.
    
MAPI_E_TOO_COMPLEX 
  
> O provedor de serviços não suporta os critérios de pesquisa especificado.
    
## <a name="remarks"></a>Coment�rios

O método **IMAPIContainer::SetSearchCriteria** estabelece critérios de pesquisa para um contêiner que suporta pesquisas, geralmente, uma pasta de resultados de pesquisa. Uma pasta de resultados de pesquisa contém links para as mensagens que atendam aos critérios de pesquisa; as mensagens reais ainda são armazenadas em seus locais originais. Os dados somente exclusivos que estão contidos em uma pasta de resultados de pesquisa são sua tabela de conteúdo. A tabela de conteúdo de uma pasta de resultados de pesquisa tem o conteúdo mesclado o armazenamento de mensagens depois que tiver sido aplicada a restrição de pesquisa. 
  
Uma operação de pesquisa funciona somente nesta tabela mescladas conteúdo; ele não procura por meio de outras pastas de resultados de pesquisa. Os resultados da pesquisa retornam somente as mensagens que correspondem aos critérios de pesquisa; a hierarquia de pastas não será retornada.
  
Controle é retornado ao cliente quando a conclusão da pesquisa.
  
## <a name="notes-to-implementers"></a>Notas para implementadores

Contêineres de catálogo de endereços estabelecer critérios de pesquisa aplicando restrições ao suas tabelas de conteúdo. Para obter mais informações sobre os critérios de pesquisa e contêineres do catálogo de endereços, consulte [Implementando a pesquisa avançada](implementing-advanced-searching.md).
  
Você deve suportar open, copiar, mover e excluir operações em todas as mensagens em pastas de resultados da pesquisa, não na pasta de resultados de pesquisa em si. Não permitir que as mensagens sejam criados dentro ou copiados para uma pasta de resultados de pesquisa. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Para pesquisar os destinatários da mensagem, defina _lpRestriction_ para apontar para uma restrição subobjeto com o membro **ulSubObject** na estrutura de [SSubRestriction](ssubrestriction.md) definida como **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)). Para procurar anexos, defina o membro **ulSubObject** como **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)). Defina o membro **lpRes** para apontar para uma restrição de propriedade que descreve os critérios de pesquisa para os destinatários ou anexos. 
  
Por exemplo, para procurar anexos de arquivo com a extensão .mss, defina **ulSubObject** **PR_MESSAGE_ATTACHMENTS** e **lpRes** para uma restrição de propriedade que corresponda **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md) ) com. mss.
  
Definir o sinalizador FOREGROUND_SEARCH no parâmetro _ulSearchFlags_ pode causar uma diminuição no desempenho do sistema. 
  
Você pode usar **definir SetSearchCriteria** para alterar os critérios de pesquisa de uma pesquisa já está em andamento. Você pode especificar novas restrições, novas listas de pastas a serem pesquisadas e uma nova prioridade de pesquisa, como atualizar uma pesquisa para uma prioridade mais alta. Alterações na ordem de prioridade de pesquisa não farão com que uma pesquisa existente reiniciar, mas podem outras alterações aos critérios de pesquisa. 
  
Quando você estiver por meio do uso de uma pasta de resultados de pesquisa, você pode excluir a pasta ou deixá-lo a permanecer abertas para uso posterior. Se você excluir a pasta de resultados de pesquisa, somente os links de mensagem serão excluídos. As mensagens reais permanecem em suas pastas pai. 
  
Para obter mais informações sobre as pastas de resultados da pesquisa, consulte [Pastas de pesquisa de MAPI](mapi-search-folders.md). 
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|HierarchyTableDlg.cpp  <br/> |CHierarchyTableDlg::OnEditSearchCriteria  <br/> |MFCMAPI usa o método **IMAPIContainer::SetSearchCriteria** para gravar os critérios de pesquisa para uma pasta depois que um usuário tenha editado-lo.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md)
  
[IMAPIContainer::OpenEntry](imapicontainer-openentry.md)
  
[IMAPIFolder::CreateFolder](imapifolder-createfolder.md)
  
[IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md)
  
[SPropertyRestriction](spropertyrestriction.md)
  
[SRestriction](srestriction.md)
  
[SSubRestriction](ssubrestriction.md)
  
[IMAPIContainer: IMAPIProp](imapicontainerimapiprop.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

