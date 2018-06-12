---
title: DNTBL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 77835b48-43aa-8518-9712-754e84f1e713
description: '�ltima altera��o: quinta-feira, 5 de julho de 2012'
ms.openlocfilehash: 6096118d72dfc51fb60025a55f581ebf97b000a7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766459"
---
# <a name="dntbl"></a>DNTBL
 
**Aplica-se a**: Outlook 
  
Informações para baixar o conteúdo de uma pasta do servidor durante a [baixar o estado da tabela](download-table-state.md), como parte de uma sincronização completa para conteúdo em um repositório.
  
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
    
    - [in] Download teve êxito. O cliente define esta após fazer o download de informações do servidor.
    
_pstmReserved1_
  
> [out] Este membro é reservado para uso interno do Outlook e não é suportado. 
    
_pstmReserved2_
  
> [out] Este membro é reservado para uso interno do Outlook e não é suportado. 
    
_pstmReserved3_
  
> [out] Este membro é reservado para uso interno do Outlook e não é suportado. 
    
_pstmReserved4_
  
> [out] Este membro é reservado para uso interno do Outlook e não é suportado. 
    
_pxicc_
  
>  [out] Ponteiro para a interface de conteúdo **IExchangeImportContentsChanges** que suporta o download de alterações de conteúdo. Para obter mais informações sobre **IExchangeImportContentsChanges**, consulte [ICS critérios de avaliação](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).
    
_pxihc_
  
>  [out] Ponteiro para a interface de hierarquia de **IExchangeImportHierarchyChanges** que suporta o download de alterações incrementais de hierarquia. Para obter mais informações sobre **IExchangeImportHierarchyChanges**, consulte [ICS critérios de avaliação](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).
    
_pszName_
  
>  [out] Nome da pasta. 
    
_ftLastMod_
  
>  [out] Hora da última modificação da pasta. 
    
_ulRights_
  
>  [out] Valor da propriedade **[PR_RIGHTS](http://msdn.microsoft.com/en-us/library/ee238052%28v=EXCHG.80%29.aspx)** da pasta. 
    
_feid_
  
>  [out] Identificação de entrada da pasta. 
    
_uintReserved_
  
>  [out] Este membro é reservado para uso interno do Outlook e não é suportado. 
    
_rgte_
  
> [out] Alterações para normal (ou não ocultos) e os itens associados (ou ocultos).  *rgte [0]* é para itens normais e *rgte [1]* é para itens associados. Outlook preenche este membro durante o download ao usar a sincronização de alteração Incremental (ICS). Para obter mais informações sobre ICS, consulte [ICS critérios de avaliação](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).
    
_lpsrReserved_
  
>  [in] / [out] este membro é reservado para uso interno do Outlook e não é suportado. 
    
_boReserved_
  
>  [in] Este membro é reservado para uso interno do Outlook e não é suportado. 
    
_pReserved1_
  
>  [out] Este membro é reservado para uso interno do Outlook e não é suportado. 
    
_pReserved2_
  
>  [in] Este membro é reservado para uso interno do Outlook e não é suportado. 
    
## <a name="see-also"></a>Confira também

- [Sobre a máquina de estado de replicação](about-the-replication-state-machine.md)  
- [Constantes MAPI](mapi-constants.md) 
- [DNTBLE](dntble.md)

