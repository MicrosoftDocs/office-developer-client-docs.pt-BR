---
title: UPTBL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 39d9ad3b-ff4b-8378-a3ac-d5621c7ef7f1
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: bdfabdf02fc0fa6222418bd0fb87e9b6c17d936a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580436"
---
# <a name="uptbl"></a>UPTBL

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Informações para carregar o conteúdo de uma pasta durante a [carregar o estado da tabela](upload-table-state.md).
  
## <a name="quick-info"></a>Informações rápidas

```cpp
struct UPTBL 
{ 
    ULONG ulFlags; 
    LPSTREAM pstmReserved; 
    LPSTR pszName; 
    FEID feid; 
    UINT uintReserved; 
    UPTBLE rgte[2]; 
    UINT iEnt; 
    UINT cEnt; 
    PUPMOV pupmovHead; 
    void* pReserved; 
};
```

## <a name="members"></a>Members

_ulFlags_
  
> [in] Sinalizadores para determinar o comportamento apropriado durante o carregamento.
    
  - UPT_OK
    
    - [in] Carregamento foi bem-sucedida. O cliente define esta após carregar o conteúdo da pasta no servidor.
    
_pstmReserved_
  
> [out] Este membro é reservado para uso interno do Outlook e não é suportado. 
    
_pszName_
  
> [out] Nome da pasta.
    
_feid_
  
> [out] Identificação de entrada da pasta.
    
_uintReserved_
  
> [out] Este membro é reservado para uso interno do Outlook e não é suportado. 
    
_rgte_
  
> [out] Estrutura para armazenar as seguintes informações para itens de normais (ou não ocultos) e os itens associados (ou ocultos) na pasta: _rgte [0]_ é para itens normais e _rgte [1]_ é para itens associados. 
    
   - o número de itens de novos ou modificados
   - o número de itens de leitura 
   - o número de itens excluídos
    
 _iEnt_
  
> [out] Índice para rastrear carregando o número de alterações especificado pelo _cEnt_.
    
_cEnt_
  
> [out] Número de alterações para a pasta.
    
_pupmovHead_
  
> [out] Cadeia de estruturas [UPMOV](upmov.md) . 
    
_Preservadas_
  
> [out] Este membro é reservado para uso interno do Outlook e não é suportado.
    
## <a name="see-also"></a>Confira também

- [Sobre a API de replicação](about-the-replication-api.md)
- [Sobre a máquina de estado de replicação](about-the-replication-state-machine.md)
- [Constantes MAPI](mapi-constants.md)
- [UPTBLE](uptble.md)

