---
title: IMAPITableGetCollapseState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.GetCollapseState
api_type:
- COM
ms.assetid: fd4ea496-4c83-49cd-854e-f373cc1ed2af
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 97575a65cd6825e07d6f11c813beec539f99f53a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436073"
---
# <a name="imapitablegetcollapsestate"></a>IMAPITable::GetCollapseState

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Retorna os dados necessários para recriar o estado recolhido ou expandido atual de uma tabela categorizada.
  
```cpp
HRESULT GetCollapseState(
ULONG ulFlags,
ULONG cbInstanceKey,
LPBYTE lpbInstanceKey,
ULONG FAR * lpcbCollapseState,
LPBYTE FAR * lppbCollapseState
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> Reservado; deve ser zero.
    
 _cbInstanceKey_
  
> [in] A contagem de bytes na chave de instância apontada pelo _parâmetro lpbInstanceKey._ 
    
 _lpbInstanceKey_
  
> [in] Um ponteiro para **a PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) da linha na qual o estado recolhido ou expandido atual deve ser reconstruído. O  _parâmetro lpbInstanceKey_ não pode ser NULL. 
    
 _lpcbCollapseState_
  
> [out] Um ponteiro para a contagem de estruturas apontadas pelo _parâmetro lppbCollapseState._ 
    
 _lppbCollapseState_
  
> [out] Um ponteiro para um ponteiro para estruturas que contêm dados que descrevem a exibição de tabela atual.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O estado da tabela categorizada foi salvo com êxito.
    
MAPI_E_BUSY 
  
> Outra operação está em andamento que impede o início da operação. A operação em andamento deve ter permissão para ser concluída ou deve ser interrompida.
    
MAPI_E_NO_SUPPORT 
  
> A tabela não suporta categorização e exibições expandidas e recolhidos.
    
## <a name="remarks"></a>Comentários

O **método IMAPITable::GetCollapseState** funciona com o método [IMAPITable::SetCollapseState](imapitable-setcollapsestate.md) para alterar o modo de exibição do usuário de uma tabela categorizada. **GetCollapseState** salva os dados necessários para **SetCollapseState** ser usado para recriar as exibições apropriadas das categorias de uma tabela categorizada. Os provedores de serviços determinam os dados a serem salvos. No entanto, a maioria dos provedores de serviços **implementando GetCollapseState** salva o seguinte: 
  
- As chaves de classificação (colunas padrão e colunas de categoria).
    
- Informações sobre a linha que a chave de instância representa.
    
- Informações para restaurar as categorias recolhidos e expandidos da tabela.
    
Para obter mais informações sobre tabelas categorizadas, consulte [Classificação e Categorização.](sorting-and-categorization.md)
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Armazene o estado atual de todos os nós de uma tabela no _parâmetro lppbCollapseState._ 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Sempre chame **GetCollapseState** antes de chamar **SetCollapseState**. 
  
## <a name="see-also"></a>Confira também



[IMAPITable::SetCollapseState](imapitable-setcollapsestate.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

