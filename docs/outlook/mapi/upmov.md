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
  
Informações para carregar itens que foram movidos. Essas informações são usadas durante o [carregamento do status de exclusão](upload-delete-status-state.md) e o [estado da tabela de carregamento](upload-table-state.md).
  
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
  
> no Sinalizadores para determinar o comportamento apropriado durante o carregamento.
    
  - UPV_ERROR
    
    - no Problema ao abrir a pasta do servidor.
    
  - UPV_DIRTY
    
    - no O estado de carregamento foi alterado. Isso é usado pelo cliente para rastrear a alteração no estado do repositório local.
    
  - UPV_COMMIT
    
    - no Confirme o estado de carregamento.
    
_Enquanto_
  
>  [out] Esse membro é reservado para uso interno do Outlook e não tem suporte. 
    
_pstmReserved_
  
>  [uto] Esse membro é reservado para uso interno do Outlook e não tem suporte. 
    
_pszName_
  
>  bota Nome da pasta de destino. 
    
  > [!NOTE]
  > Este membro não dá suporte a UNICODE. 
  
_feid_
  
>  bota ID de entrada da pasta de destino. 
    
_pfld_
  
>  no Ponteiro para a pasta do servidor. 
    
_pxicc_
  
>  no Ponteiro para a interface de conteúdo do **IExchangeImportContentsChanges** que oferece suporte ao carregamento de alterações de conteúdo ao usar a sincronização de alteração incremental (ICS). Para obter mais informações sobre o **IExchangeImportContentsChanges** e o ICS, consulte [critérios de avaliação de ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).
    
_dwReserved_
  
>  [out] Esse membro é reservado para uso interno do Outlook e não tem suporte. 
    
_pupmovNext_
  
>  bota Próximo contexto de movimentação. 
    
_cEntMov_
  
>  no Número de itens movidos aqui. 
    
## <a name="see-also"></a>Confira também

- [Sobre a API de replicação](about-the-replication-api.md)
- [Sobre a máquina de estado de replicação](about-the-replication-state-machine.md)
- [Constantes de MAPI](mapi-constants.md)
- [FEID](feid.md)

