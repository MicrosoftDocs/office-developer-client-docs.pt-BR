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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 2c1246c46e9723cd3f6d92f0a44fc1419eef4a2e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767321"
---
# <a name="imapitablegetcollapsestate"></a>IMAPITable::GetCollapseState

  
  
**Aplica-se a**: Outlook 
  
Retorna os dados que não é necessário para reconstruir atual recolhido ou expandido o estado de uma tabela categorizado.
  
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
  
> [in] A contagem de bytes na chave instância apontado pelo parâmetro _lpbInstanceKey_ . 
    
 _lpbInstanceKey_
  
> [in] Um ponteiro para a propriedade **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) da linha no qual as atuais recolhido ou expandida estado deve ser recriado. O parâmetro _lpbInstanceKey_ não pode ser NULL. 
    
 _lpcbCollapseState_
  
> [out] Um ponteiro para a contagem de estruturas apontado pelo parâmetro _lppbCollapseState_ . 
    
 _lppbCollapseState_
  
> [out] Um ponteiro para um ponteiro para estruturas que contenham dados que descreve o modo de exibição de tabela atual.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> O estado da tabela categorizado foi salvo com êxito.
    
MAPI_E_BUSY 
  
> Outra operação está em andamento que impede que a operação seja iniciado. Ou a operação em andamento deve ter permissão para concluir ou ele deve ser interrompido.
    
MAPI_E_NO_SUPPORT 
  
> A tabela não oferece suporte a categorização e exibições expandida e recolhida.
    
## <a name="remarks"></a>Comentários

O método **IMAPITable::GetCollapseState** funciona com o método [IMAPITable::SetCollapseState](imapitable-setcollapsestate.md) para alterar o modo de exibição do usuário de uma tabela categorizado. **GetCollapseState** salva os dados que é necessário para **SetCollapseState** será usado para reconstruir os modos de exibição apropriados das categorias de uma tabela categorizada. Provedores de serviços de determinam os dados a serem salvos. No entanto, a maioria dos provedores de serviço implementando **GetCollapseState** salvar o seguinte: 
  
- As chaves de classificação (standard colunas e colunas de categoria).
    
- Informações sobre a linha que representa a chave da instância.
    
- Informações para restaurar as categorias expandidas e recolhidas da tabela.
    
Para obter mais informações sobre tabelas categorizadas, consulte [classificação e categorização](sorting-and-categorization.md).
  
## <a name="notes-to-implementers"></a>Notas para implementadores

Armazene o estado atual de todos os nós de uma tabela no parâmetro _lppbCollapseState_ . 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Sempre chame **GetCollapseState** antes de chamar **SetCollapseState**. 
  
## <a name="see-also"></a>Confira também



[IMAPITable::SetCollapseState](imapitable-setcollapsestate.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

