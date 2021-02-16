---
title: HrValidateIPMSubtree
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrValidateIPMSubtree
api_type:
- COM
ms.assetid: 6454c1fa-5216-4934-a908-48c634ac4a07
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 6cf51985e534434c584eff4d63dfbf239121ee85
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436570"
---
# <a name="hrvalidateipmsubtree"></a>HrValidateIPMSubtree

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Adiciona pastas de mensagens padrão interpersonal (IPM) a um armazenamento de mensagens. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos do cliente  <br/> |
   
```cpp
HrValidateIPMSubtree(
  LPMDB lpMDB,
  ULONG ulFlags,
  ULONG FAR * lpcValues,
  LPSPropValue FAR * lppProps,
  LPMAPIERROR FAR * lppMapiError
);
```

## <a name="parameters"></a>Parâmetros

 _lpMDB_
  
> [in] Ponteiro para o objeto de armazenamento de mensagens ao qual adicionar as pastas. 
    
 _ulFlags_
  
> [in] Bitmask de sinalizadores usados para controlar como as pastas são criadas. Os sinalizadores a seguir podem ser definidos:
    
MAPI_FORCE_CREATE 
  
> As pastas devem ser verificadas antes da criação, mesmo se as propriedades do armazenamento de mensagens indicarem que são válidas. Um aplicativo cliente normalmente define esse sinalizador quando um erro indica que a estrutura de uma pasta existente foi danificada. 
    
MAPI_FULL_IPM_TREE 
  
> O conjunto completo de pastas IPM deve ser criado na pasta raiz do armazenamento de mensagens. Os títulos de pasta na hierarquia são:
    
    - Exibições de Pasta
    
    - Exibições comuns
    
    - Raiz de Pesquisa\*
    
    - Subárvore IPM\*
    
    - Caixa de Entrada
    
    - Caixa de saída
    
    - Itens excluídos\*
    
    - Itens enviados
    
    onde as três pastas marcadas com são o conjunto mínimo criado mesmo quando o \* MAPI_FULL_IPM_TREE sinalizador não foi definido. Um aplicativo cliente normalmente define esse sinalizador quando o armazenamento de mensagens no qual as pastas devem ser criadas é o armazenamento padrão.
    
 _lpcValues_
  
> [in, out] Ponteiro para o número de [estruturas SPropValue](spropvalue.md) na matriz retornada no _parâmetro lppProps._ O valor do parâmetro  _lpcValues_ pode ser zero se  _lppProps_ for NULL. 
    
 _lppProps_
  
> [in, out] Ponteiro para um ponteiro para uma matriz de **estruturas SPropValue** que contém valores de propriedade para a propriedade **PR_VALID_FOLDER_MASK** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md)) e para as propriedades de identificador de entrada de pasta apropriadas. Se **HrValidateIPMSubtree** criar uma Caixa de Entrada no armazenamento de mensagens, a matriz **SPropValue** incluirá um identificador de entrada de Caixa de Entrada com uma marca de propriedade especial codificada como  `PROP_TAG(PT_BINARY, PROP_ID_NULL)` . O  _parâmetro lppProps_ pode ser NULL, indicando que a implementação da chamada não exige que uma **matriz SPropValue** seja retornada. 
    
 _lppMapiError_
  
> [out] Ponteiro para um ponteiro para uma [estrutura MAPIERROR](mapierror.md) que contém informações de versão, componente e contexto para um erro. O  _parâmetro lppMAPIError_ é definido como NULL se nenhuma **estrutura MAPIERROR** for retornada. 
    
## <a name="return-value"></a>Valor retornado

Nenhum.
  
## <a name="remarks"></a>Comentários

MAPI uses the **HrValidateIPMSubtree** function internally to construct the standard IPM subtree in a message store when the store is first opened, or when a store is made the default store. Essa função também pode ser usada por aplicativos cliente para validar ou reparar pastas de mensagens padrão. 
  
 **HrValidateIPMSubtree** sempre cria as pastas Raiz de Pesquisa e Subárvore do IPM na pasta raiz do armazenamento e a pasta Itens Excluídos na pasta Subárvore do IPM. A pasta Subárvore do IPM é a raiz da hierarquia do IPM nesse armazenamento de mensagens. A pasta Raiz da Pesquisa pode ser usada como raiz de uma subárvore para pastas de resultados de pesquisa. 
  
Os clientes IPM devem exibir a exibição de pastas começando na pasta raiz da subárvore do IPM e mostrando pastas filho abaixo dela. As informações na pasta raiz de um armazenamento de mensagens não devem aparecer na interface do usuário de um cliente. Essa funcionalidade significa que, se um cliente tiver que ocultar informações, as informações poderão ser colocadas no diretório raiz da subárvore do IPM, onde não estarão visíveis para o usuário. Por outro lado, aplicativos não IPM que exigem que mensagens e pastas sejam invisíveis para o usuário, por exemplo, em um armazenamento de mensagens baseado em servidor, podem colocá-los fora da hierarquia do IPM. 
  
 **HrValidateIPMSubtree** define a propriedade **PR_VALID_FOLDER_MASK** para indicar se cada pasta IPM criada tem um identificador de entrada válido. As seguintes propriedades do identificador de entrada do armazenamento de mensagens são definidas para os identificadores de entrada das pastas correspondentes e retornadas no parâmetro  _lppProps_ juntamente com **PR_VALID_FOLDER_MASK**: 
  
 **PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md))
  
> **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md))
  
> **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md))
  
> **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))
  
> **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))
  
> **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))
  
> **PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md))
  
> Um espaço reservado [PROP_TAG](prop_tag.md) para a Caixa de Entrada do IPM (PT_BINARY, PROP_ID_NULL). 
    
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MstStoreDlg.cpp  <br/> |CMsgStoreDlg::OnValidateIPMSubtree  <br/> |MFCMAPI usa o **método HrValidateIPMSubtree** para adicionar pastas padrão a um armazenamento de mensagens.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

