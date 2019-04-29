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
  
Adiciona pastas padrão de mensagens interpessoais (IPM) a um repositório de mensagens. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente  <br/> |
   
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
  
> no Ponteiro para o objeto do repositório de mensagens ao qual as pastas serão adicionadas. 
    
 _ulFlags_
  
> no Bitmask dos sinalizadores usados para controlar como as pastas são criadas. Os seguintes sinalizadores podem ser definidos:
    
MAPI_FORCE_CREATE 
  
> As pastas devem ser verificadas antes da criação, mesmo se as propriedades do repositório de mensagens indicarem que são válidas. Um aplicativo cliente normalmente define esse sinalizador quando um erro indica que a estrutura de uma pasta existente foi danificada. 
    
MAPI_FULL_IPM_TREE 
  
> O conjunto completo de pastas IPM deve ser criado na pasta raiz do repositório de mensagens. Os títulos de pasta na hierarquia são:
    
    - Modos de exibição de pasta
    
    - Modos de exibição comuns
    
    - Raiz de pesquisa\*
    
    - SubÁrvore IPM\*
    
    - Caixa de Entrada
    
    - Enviada
    
    - Itens excluídos\*
    
    - Itens enviados
    
    onde as três pastas marcadas \* com são o conjunto mínimo criado, mesmo quando o sinalizador MAPI_FULL_IPM_TREE não foi definido. Um aplicativo cliente normalmente define esse sinalizador quando o repositório de mensagens no qual as pastas devem ser criadas é o repositório padrão.
    
 _lpcValues_
  
> [in, out] Ponteiro para o número de estruturas [SPropValue](spropvalue.md) na matriz retornada no parâmetro _lppProps_ . O valor do parâmetro _lpcValues_ pode ser zero se _lppProps_ for nulo. 
    
 _lppProps_
  
> [in, out] Ponteiro para um ponteiro para uma matriz de estruturas **SPropValue** que contém valores de propriedade para a propriedade **PR_VALID_FOLDER_MASK** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md)) e para as propriedades de identificador de entrada de pasta apropriadas. Se **HrValidateIPMSubtree** cria uma caixa de entrada no repositório de mensagens, a matriz **SPropValue** inclui um identificador de entrada de caixa de entrada com uma `PROP_TAG(PT_BINARY, PROP_ID_NULL)`marca de propriedade especial codificada como. O parâmetro _lppProps_ pode ser NULL, indicando que a implementação de chamada não exige que uma matriz **SPropValue** seja retornada. 
    
 _lppMapiError_
  
> bota Ponteiro para um ponteiro para uma estrutura [MAPIERROR](mapierror.md) que contém a versão, o componente e informações de contexto de um erro. O parâmetro _lppMAPIError_ é definido como NULL se nenhuma estrutura **MAPIERROR** for retornada. 
    
## <a name="return-value"></a>Valor retornado

Nenhum.
  
## <a name="remarks"></a>Comentários

MAPI usa a função **HrValidateIPMSubtree** internamente para construir a subárvore IPM padrão em um repositório de mensagens quando o repositório é aberto pela primeira vez ou quando um repositório é tornado o repositório padrão. Essa função também pode ser usada por aplicativos cliente para validar ou reparar pastas de mensagens padrão. 
  
 O **HrValidateIPMSubtree** sempre cria as pastas de subárvores de pesquisa e de raiz IPM na pasta raiz do repositório e na pasta itens excluídos na pasta IPM Tree. A pasta de sub-árvore IPM é a raiz da hierarquia IPM no repositório de mensagens. A pasta raiz de pesquisa pode ser usada como a raiz de uma subárvore para pastas de resultados de pesquisa. 
  
Os clientes IPM devem exibir o modo de exibição de pastas começando na pasta raiz da sub-árvore IPM e mostrando as pastas filhas abaixo dela. As informações na pasta raiz de um repositório de mensagens não devem aparecer na interface de usuário de um cliente. Essa funcionalidade significa que, se um cliente deve ocultar informações, as informações podem ser colocadas no diretório raiz da sub-árvore IPM, onde não fica visível para o usuário. Por outro lado, aplicativos não-IPM que exigem mensagens e pastas invisíveis para o usuário, por exemplo, em um repositório de mensagens baseado em servidor, podem colocá-los fora da hierarquia IPM. 
  
 **HrValidateIPMSubtree** define a propriedade **PR_VALID_FOLDER_MASK** para indicar se cada pasta IPM que ele cria tem um identificador de entrada válido. As seguintes propriedades de identificador de entrada do repositório de mensagens são definidas para os identificadores de entrada das pastas correspondentes e retornadas no parâmetro _lppProps_ juntamente com **PR_VALID_FOLDER_MASK**: 
  
 **PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md))
  
> **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md))
  
> **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md))
  
> **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))
  
> **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))
  
> **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))
  
> **PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md))
  
> Uma [PROP_TAG](prop_tag.md) de espaço reservado para a caixa de entrada IPM (PT_BINARY, PROP_ID_NULL). 
    
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MstStoreDlg. cpp  <br/> |CMsgStoreDlg:: OnValidateIPMSubtree  <br/> |MFCMAPI usa o método **HrValidateIPMSubtree** para adicionar pastas padrão a um repositório de mensagens.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

