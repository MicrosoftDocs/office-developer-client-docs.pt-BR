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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328922"
---
# <a name="imapitablegetcollapsestate"></a>IMAPITable::GetCollapseState

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Retorna os dados necessários para reconstruir o estado atual recolhido ou expandido de uma tabela categorizada.
  
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
  
> Serve deve ser zero.
    
 _cbInstanceKey_
  
> no A contagem de bytes na chave de instância indicada pelo parâmetro _lpbInstanceKey_ . 
    
 _lpbInstanceKey_
  
> no Um ponteiro para a propriedade **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) da linha na qual o estado atual recolhido ou expandido deve ser recriado. O parâmetro _lpbInstanceKey_ não pode ser nulo. 
    
 _lpcbCollapseState_
  
> bota Um ponteiro para a contagem de estruturas apontada pelo parâmetro _lppbCollapseState_ . 
    
 _lppbCollapseState_
  
> bota Um ponteiro para um ponteiro para estruturas que contêm dados que descrevem o modo de exibição de tabela atual.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O estado da tabela categorizada foi salvo com êxito.
    
MAPI_E_BUSY 
  
> Outra operação está em andamento, o que impede a inicialização da operação. A operação em andamento deve ter permissão para ser concluída ou deve ser interrompida.
    
MAPI_E_NO_SUPPORT 
  
> A tabela não dá suporte a categorização e exibições expandidas e recolhidas.
    
## <a name="remarks"></a>Comentários

O método imApitable **::** getcollapsestate funciona com o método IMAPITable [::](imapitable-setcollapsestate.md) setcollapsestate para alterar o modo de exibição do usuário de uma tabela categorizada. **** Getcollapsestate salva os dados necessários para setcollapsestate a ser usado para reconstruir as exibições apropriadas das categorias de uma tabela categorizada. **** Os provedores de serviços determinam os dados a serem salvos. No enTanto, a maioria **** dos provedores de serviços que implementam getcollapsestate salvam o seguinte: 
  
- As chaves de classificação (colunas de categoria e colunas padrão).
    
- Informações sobre a linha que a chave de instância representa.
    
- Informações para restaurar as categorias recolhidas e expandidas da tabela.
    
Para obter mais informações sobre tabelas categorizadas, consulte [classificação e categorização](sorting-and-categorization.md).
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Armazenar o estado atual de todos os nós de uma tabela no parâmetro _lppbCollapseState_ . 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Chame sempre **** getcollapsestate antes de chamar **** setcollapsestate. 
  
## <a name="see-also"></a>Confira também



[IMAPITable::SetCollapseState](imapitable-setcollapsestate.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

