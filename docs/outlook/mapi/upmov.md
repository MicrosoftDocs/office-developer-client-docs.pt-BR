---
title: UPMOV
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 098743a5-f265-639a-8ba6-1412705bee0a
description: '�ltima altera��o: quinta-feira, 5 de julho de 2012'
ms.openlocfilehash: 0a8e318f9bb5e538473e1b60c650e8730f692e50
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577986"
---
# <a name="upmov"></a>UPMOV
 
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Informações de carregamento de itens que foram movidos. Essas informações são usadas durante o [carregamento excluir o estado de status](upload-delete-status-state.md) e [carregar o estado da tabela](upload-table-state.md).
  
## <a name="quick-info"></a>Informações rápidas

```cpp
struct UPMOV 
{ 
      ULONG          ulFlags; 
      LPVOID         pReserved; 
      LPSTREAM       pstmReserved; 
      LPSTR          pszName; 
      FEID           feid; 
      LPMAPIFOLDER   pfld; 
      PXICC          pxicc; 
      DWORD          dwReserved; 
      PUPMOV         pupmovNext; 
      UINT           cEntMov; 
};
```

## <a name="members"></a>Members

_ulFlags_
  
> [in] Sinalizadores para determinar o comportamento apropriado durante o carregamento.
    
  - UPV_ERROR
    
    - [in] Problema ao abrir a pasta do servidor.
    
  - UPV_DIRTY
    
    - [in] O estado de carregamento foi alterada. Isso é usado pelo cliente para rastrear a alteração do estado de armazenamento local.
    
  - UPV_COMMIT
    
    - [in] Confirme o estado de carregamento.
    
_Preservadas_
  
>  [out] Este membro é reservado para uso interno do Outlook e não é suportado. 
    
_pstmReserved_
  
>  [out] Este membro é reservado para uso interno do Outlook e não é suportado. 
    
_pszName_
  
>  [out] Nome da pasta de destino. 
    
  > [!NOTE]
  > Este membro não oferece suporte a UNICODE. 
  
_feid_
  
>  [out] Identificação de entrada da pasta de destino. 
    
_pfld_
  
>  [in] Ponteiro para a pasta do servidor. 
    
_pxicc_
  
>  [in] Ponteiro para a interface de conteúdo de **IExchangeImportContentsChanges** que ofereça suporte a carregamento de alterações de conteúdo ao usar a sincronização de alteração Incremental (ICS). Para obter mais informações sobre **IExchangeImportContentsChanges** e ICS, consulte [ICS critérios de avaliação](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).
    
_dwReserved_
  
>  [out] Este membro é reservado para uso interno do Outlook e não é suportado. 
    
_pupmovNext_
  
>  [out] Em seguida, mova contexto. 
    
_cEntMov_
  
>  [in] Número de itens movidos aqui. 
    
## <a name="see-also"></a>Confira também

- [Sobre a API de replicação](about-the-replication-api.md)
- [Sobre a máquina de estado de replicação](about-the-replication-state-machine.md)
- [Constantes MAPI](mapi-constants.md)
- [FEID](feid.md)

