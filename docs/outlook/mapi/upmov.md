---
title: UPMOV
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 098743a5-f265-639a-8ba6-1412705bee0a
description: 'Última modificação: 05 de julho de 2012'
ms.openlocfilehash: a7588d5fed2e059be7e628d8a76a12f76aea734d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393380"
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

## <a name="members"></a>Membros

_ulFlags_
  
> [in] Sinalizadores para determinar o comportamento apropriado durante o carregamento.
    
  - UPV_ERROR
    
    - [in] Problema ao abrir a pasta do servidor.
    
  - UPV_DIRTY
    
    - [in] O estado de carregamento foi alterada. Isso é usado pelo cliente para rastrear a alteração do estado de armazenamento local.
    
  - UPV_COMMIT
    
    - [in] Confirme o estado de carregamento.
    
_Preservadas_
  
>  [out] Esse membro é reservado para uso interno do Outlook e não tem suporte. 
    
_pstmReserved_
  
>  [uto] Esse membro é reservado para uso interno do Outlook e não tem suporte. 
    
_pszName_
  
>  [out] Nome da pasta de destino. 
    
  > [!NOTE]
  > Este membro não oferece suporte a UNICODE. 
  
_feid_
  
>  [out] Identificação de entrada da pasta de destino. 
    
_pfld_
  
>  [in] Ponteiro para a pasta do servidor. 
    
_pxicc_
  
>  [in] Ponteiro para a interface de conteúdo de **IExchangeImportContentsChanges** que ofereça suporte a carregamento de alterações de conteúdo ao usar a sincronização de alteração Incremental (ICS). Para obter mais informações sobre **IExchangeImportContentsChanges** e ICS, consulte [ICS critérios de avaliação](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).
    
_dwReserved_
  
>  [out] Esse membro é reservado para uso interno do Outlook e não tem suporte. 
    
_pupmovNext_
  
>  [out] Em seguida, mova contexto. 
    
_cEntMov_
  
>  [in] Número de itens movidos aqui. 
    
## <a name="see-also"></a>Confira também

- [Sobre a API de replicação](about-the-replication-api.md)
- [Sobre a máquina de estado de replicação](about-the-replication-state-machine.md)
- [Constantes de MAPI](mapi-constants.md)
- [FEID](feid.md)

