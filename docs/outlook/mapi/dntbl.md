---
title: DNTBL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 77835b48-43aa-8518-9712-754e84f1e713
description: 'Última modificação: 05 de julho de 2012'
ms.openlocfilehash: 4716a6f42968d7451a5db36173c4e6a9e843c08e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398119"
---
# <a name="dntbl"></a>DNTBL
 
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Informações para baixar o conteúdo de uma pasta do servidor durante o [estado de download de tabela](download-table-state.md), como parte de uma sincronização completa do conteúdo de um repositório.
  
## <a name="quick-info"></a>Informações rápidas

```cpp
struct DNTBL 
{ 
    ULONG ulFlags; 
    LPSTREAM pstmReserved1; 
    LPSTREAM pstmReserved2; 
    LPSTREAM pstmReserved3; 
    LPSTREAM pstmReserved4; 
    PXICC pxicc; 
    PXIHC pxihc; 
    LPSTR pszName; 
    FILETIME ftLastMod; 
    ULONG ulRights; 
    FEID feid; 
    UINT uintReserved; 
    DNTBLE rgte[2]; 
    LPSRestriction psrReserved; 
    BOOL boReserved; 
    void* pReserved1; 
    void* pReserved2; 
};

```

## <a name="members"></a>Membros

_ulFlags_
  
> [in] Sinalizadores para modificar o comportamento 
    
  - DNT_OK
    
    - [in] Download bem-sucedido. O cliente define isso depois de baixar informações do servidor.
    
_pstmReserved1_
  
> [out] Esse membro é reservado para uso interno do Outlook e não tem suporte. 
    
_pstmReserved2_
  
> [out] Esse membro é reservado para uso interno do Outlook e não tem suporte. 
    
_pstmReserved3_
  
> [out] Esse membro é reservado para uso interno do Outlook e não tem suporte. 
    
_pstmReserved4_
  
> [out] Esse membro é reservado para uso interno do Outlook e não tem suporte. 
    
_pxicc_
  
>  [out] Ponteiro para a interface de conteúdo **IExchangeImportContentsChanges** que suporta o download de alterações de conteúdo. Para saber mais sobre **IExchangeImportContentsChanges**, confira [Critérios de avaliação de ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).
    
_pxihc_
  
>  [out] Ponteiro para a interface de hierarquia **IExchangeImportHierarchyChanges** que suporta o download de alterações incrementais de hierarquia. Para saber mais sobre **IExchangeImportHierarchyChanges**, confira [Critérios de avaliação de ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).
    
_pszName_
  
>  [out] Nome da pasta. 
    
_ftLastMod_
  
>  [out] Hora da última modificação da pasta. 
    
_ulRights_
  
>  [out] Valor da propriedade ** [PR_RIGHTS](https://msdn.microsoft.com/library/ee238052%28v=EXCHG.80%29.aspx) ** da pasta. 
    
_feid_
  
>  [out] ID da entrada da pasta. 
    
_uintReserved_
  
>  [out] Esse membro é reservado para uso interno do Outlook e não tem suporte. 
    
_rgte_
  
> [out] Alterações para itens normais (ou não ocultos) e associados (ou ocultos).  *rgte[0]* destina-se a itens normais, e *rgte[1]* a itens associados. O Outlook preenche este membro durante o download ao usar a Sincronização de Alteração Incremental (ICS). Confira mais informações sobre ICS em [Critérios de avaliação de ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).
    
_lpsrReserved_
  
>  [in]/[out] Este membro é reservado para uso interno do Outlook e não tem suporte. 
    
_boReserved_
  
>  [in]Este membro é reservado para uso interno do Outlook e não tem suporte. 
    
_pReserved1_
  
>  [out] Este membro é reservado para uso interno do Outlook e não tem suporte. 
    
_pReserved2_
  
>  [in]Este membro é reservado para uso interno do Outlook e não tem suporte. 
    
## <a name="see-also"></a>Confira também

- [Sobre a máquina de estado de replicação](about-the-replication-state-machine.md)  
- [Constantes de MAPI](mapi-constants.md) 
- [DNTBLE](dntble.md)

