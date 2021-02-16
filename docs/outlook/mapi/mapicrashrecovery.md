---
title: MAPICrashRecovery
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPICrashRecovery
api_type:
- COM
ms.assetid: 4172e2d3-6343-385b-c691-a64c1e198051
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 9efafbac55a2925e04b533e7c08388c026540dff
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407211"
---
# <a name="mapicrashrecovery"></a>MAPICrashRecovery

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
A **função MAPICrashRecovery** verifica o estado da memória compartilhada do arquivo de Pastas Particulares (PST) ou do arquivo de Pastas Offline (OST). Se a memória estiver em um estado consistente, a função **MAPICrashRecovery** move os dados para o disco e impede acesso de leitura ou gravação até que o processo seja encerrado. 
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Exportado por:  <br/> |olmapi32.dll  <br/> |
|Chamado por:  <br/> |Cliente  <br/> |
|Implementado por:  <br/> |Outlook  <br/> |
   
```cpp
void MAPICrashRecovery(ULONG ulFlags);
```

## <a name="parameters"></a>Parâmetros

_ulFlags_
  
> [in] Sinalizadores usados para controlar como a recuperação de falhas MAPI é executada. Os sinalizadores a seguir podem ser definidos:
    
   - **MAPICRASH \_ RECOVER**: se os PSTs ou OSTs estão em um estado consistente, mova os dados para o disco e bloqueie os PSTs ou OSTs para impedir o acesso de leitura ou gravação.
    
   - **MAPICRASH \_ CONTINUE**: Desbloqueie os PSTs ou OSTs para depuração. Após uma chamada bem-sucedida para **MAPICrashRecovery** com o sinalizador **MAPICRASH_RECOVER,** chame **MAPICrashRecovery** com o sinalizador **CONTINUE DE MAPICRASH \_** para permitir que a depuração continue. 
    
   - **MAPICRASH \_ SYSTEM_SHUTDOWN**: se os PSTs ou OSTs estão em um estado consistente, mova os dados para o disco e bloqueie os PSTs ou OSTs para impedir o acesso de leitura ou gravação. Os PSTs ou OSTs não podem ser desbloqueados usando **MAPICRASH \_ CONTINUE**. Deve ser usado em combinação com **MAPICRASH \_ RECOVER**. 
    
## <a name="remarks"></a>Comentários

O byte superior (0xFF000000) é reservado para sinalizadores de recuperação de falhas específicos do provedor.
  
Chame **MAPICrashRecovery** com o **MAPICRASH \_ RECOVER** **e MAPICRASH_SYSTEM_SHUTDOWN** sinalizadores em resposta à WM_ENDSESSION mensagem.  
  
## <a name="see-also"></a>Confira também

- [Sobre a API de recuperação de falhas MAPI](about-the-mapi-crash-recovery-api.md)
- [Usar a API de recuperação de falhas MAPI](how-to-use-the-mapi-crash-recovery-api.md)

