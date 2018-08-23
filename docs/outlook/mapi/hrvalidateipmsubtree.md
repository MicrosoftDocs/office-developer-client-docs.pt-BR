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
ms.openlocfilehash: 2625b148d15c2f5ccf65eedf3a1b1f2c9d0d133e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592042"
---
# <a name="hrvalidateipmsubtree"></a>HrValidateIPMSubtree

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Adiciona as pastas de mensagem padrão interpessoais (IPM) para um armazenamento de mensagens. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Aplicativos cliente  <br/> |
   
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
  
> [in] Ponteiro para a mensagem armazenar o objeto ao qual adicionar as pastas. 
    
 _ulFlags_
  
> [in] Bitmask dos sinalizadores usadas para controlar como as pastas são criadas. Sinalizadores a seguir podem ser definidos:
    
MAPI_FORCE_CREATE 
  
> As pastas devem ser verificadas antes da criação, mesmo se o repositório de propriedades da mensagem indicam que eles são válidos. Um aplicativo cliente geralmente define esse sinalizador quando um erro indica que a estrutura de uma pasta existente foi danificada. 
    
MAPI_FULL_IPM_TREE 
  
> O conjunto completo de pastas IPM deve ser criado na pasta raiz do repositório de mensagem. Os títulos de pasta na hierarquia são:
    
    - Modos de exibição de pasta
    
    - Modos de exibição comuns
    
    - Raiz de pesquisa\*
    
    - Subárvore IPM\*
    
    - Caixa de Entrada
    
    - Caixa de saída
    
    - Itens excluídos\*
    
    - Itens enviados
    
    onde as três pastas marcadas com \* são o conjunto mínimo criado mesmo quando o sinalizador MAPI_FULL_IPM_TREE não foi definido. Um aplicativo cliente geralmente define esse sinalizador quando o armazenamento de mensagens em que as pastas devem ser criados é o repositório padrão.
    
 _lpcValues_
  
> [além, out] Ponteiro para o número de estruturas de [SPropValue](spropvalue.md) na matriz retornada no parâmetro _lppProps_ . O valor do parâmetro _lpcValues_ pode ser zero se _lppProps_ é NULL. 
    
 _lppProps_
  
> [além, out] Ponteiro para um ponteiro para uma matriz de estruturas de **SPropValue** que contém os valores de propriedade para a propriedade **PR_VALID_FOLDER_MASK** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md)) e as propriedades de identificador de entrada de pasta apropriada. Se **HrValidateIPMSubtree** cria uma caixa de entrada no repositório de mensagem, a matriz de **SPropValue** inclui um identificador de entrada da caixa de entrada com uma marca de propriedade especial codificada como `PROP_TAG(PT_BINARY, PROP_ID_NULL)`. O parâmetro _lppProps_ pode ser NULL, indicando que a implementação de chamada não exige que uma matriz **SPropValue** ser retornado. 
    
 _lppMapiError_
  
> [out] Ponteiro para um ponteiro para uma estrutura [MAPIERROR](mapierror.md) que contém informações de versão, componente e contexto para um erro. O parâmetro _lppMAPIError_ é definido como NULL se nenhuma estrutura **MAPIERROR** é retornada. 
    
## <a name="return-value"></a>Valor retornado

Nenhum.
  
## <a name="remarks"></a>Comentários

MAPI usa a função **HrValidateIPMSubtree** internamente para construir a subárvore IPM padrão em um repositório de mensagem quando o armazenamento é aberto pela primeira vez ou quando um repositório é feito padrão armazenar. Essa função também pode ser usada pelos aplicativos cliente para validar ou reparar as pastas de mensagem padrão. 
  
 **HrValidateIPMSubtree** sempre cria as pastas raiz de pesquisa e subárvore IPM na pasta raiz do repositório e a pasta Itens excluídos na pasta subárvore IPM. A pasta subárvore IPM é a raiz da hierarquia IPM desse repositório de mensagem. A pasta raiz de pesquisa pode ser usada como a raiz de uma subárvore para pastas de resultados de pesquisa. 
  
Clientes IPM devem exibição de suas pastas começando na pasta raiz de subárvore IPM e mostrando filho pastas sob ele. Informações na pasta raiz de um repositório de mensagem não devem aparecer na interface do usuário do cliente. Essa funcionalidade significa que se um cliente deve ocultar as informações, as informações podem ser colocadas no diretório raiz subárvore IPM, onde não é visível para o usuário. Por outro lado, os aplicativos de não-IPM que exigem mensagens e pastas invisível ao usuário, por exemplo, em um armazenamento de mensagens baseado em servidor, podem colocá-los fora da hierarquia IPM. 
  
 **HrValidateIPMSubtree** define a propriedade **PR_VALID_FOLDER_MASK** para indicar se cada pasta IPM cria tem um identificador de entrada válida. As seguintes propriedades do identificador de entrada do repositório de mensagem estiver definidas como os identificadores de entrada das pastas correspondentes e retornadas no parâmetro _lppProps_ juntamente com **PR_VALID_FOLDER_MASK**: 
  
 **PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md))
  
> **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md))
  
> **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md))
  
> **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))
  
> **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))
  
> **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))
  
> **PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md))
  
> Um espaço reservado [PROP_TAG](prop_tag.md) para a caixa de entrada IPM (PT_BINARY, PROP_ID_NULL). 
    
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|MstStoreDlg.cpp  <br/> |CMsgStoreDlg::OnValidateIPMSubtree  <br/> |MFCMAPI usa o método **HrValidateIPMSubtree** para adicionar pastas padrão para um armazenamento de mensagens.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

