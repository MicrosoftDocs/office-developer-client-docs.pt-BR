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
ms.openlocfilehash: a7588d5fed2e059be7e628d8a76a12f76aea734d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339183"
---
# <a name="upmov"></a>UPMOV
 
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Informações para carregar itens que foram movidos. Essas informações são usadas durante o estado [de status de exclusão de upload](upload-delete-status-state.md) e o estado da tabela de [carregamento.](upload-table-state.md)
  
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
    
    - [in] O estado de carregamento foi alterado. Isso é usado pelo cliente para controlar a alteração no estado do armazenamento local.
    
  - UPV_COMMIT
    
    - [in] Estado de carregamento de confirmações.
    
_pReserved_
  
>  [out] Esse membro é reservado para uso interno do Outlook e não tem suporte. 
    
_pstmReserved_
  
>  [uto] Esse membro é reservado para uso interno do Outlook e não tem suporte. 
    
_pszName_
  
>  [out] Nome da pasta de destino. 
    
  > [!NOTE]
  > Este membro não dá suporte a UNICODE. 
  
_feid_
  
>  [out] ID de entrada da pasta de destino. 
    
_pfld_
  
>  [in] Ponteiro para pasta do servidor. 
    
_pxicc_
  
>  [in] Ponteiro para a interface **de conteúdo IExchangeImportContentsChanges** que oferece suporte ao carregamento de alterações de conteúdo ao usar a Sincronização de Alteração Incremental (ICS). Para obter mais informações **sobre IExchangeImportContentsChanges** e ICS, consulte Critérios de [Avaliação do ICS.](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx)
    
_dwReserved_
  
>  [out] Esse membro é reservado para uso interno do Outlook e não tem suporte. 
    
_gnamovNext_
  
>  [out] Em seguida, mova o contexto. 
    
_cEntMov_
  
>  [in] Número de itens movidos aqui. 
    
## <a name="see-also"></a>Confira também

- [Sobre a API de replicação](about-the-replication-api.md)
- [Sobre a máquina de estado de replicação](about-the-replication-state-machine.md)
- [Constantes de MAPI](mapi-constants.md)
- [FEID](feid.md)

