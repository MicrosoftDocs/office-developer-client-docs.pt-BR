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
ms.openlocfilehash: 6b07d794a8f54477c6706cb70af60f7f7ef57d49
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595339"
---
# <a name="mapicrashrecovery"></a>MAPICrashRecovery

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
A função de **MAPICrashRecovery** verifica que o estado do arquivo de pastas particulares (. PST) ou o arquivo de pastas Offline (OST) a memória compartilhada. Se a memória estiver em um estado consistente, a função **MAPICrashRecovery** move os dados em disco e impede que o maior acesso de leitura ou gravação até que o processo é encerrado. 
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Exportá-los por:  <br/> |olmapi32.dll  <br/> |
|Chamado pelo:  <br/> |Cliente  <br/> |
|Implementada por:  <br/> |Outlook  <br/> |
   
```cpp
void MAPICrashRecovery(ULONG ulFlags);
```

## <a name="parameters"></a>Parâmetros

_ulFlags_
  
> [in] Sinalizadores usados para controlar como a recuperação de travamento MAPI é executada. Sinalizadores a seguir podem ser definidos:
    
   - **MAPICRASH\_recuperar**: se o PSTs ou OSTs estiverem em um estado consistente, mover os dados em disco e bloquear o PSTs ou OSTs para impedir o acesso de leitura ou gravação.
    
   - **MAPICRASH\_continuar**: desbloquear o PSTs ou OSTs para depuração. Após uma chamada bem sucedida para **MAPICrashRecovery** com o sinalizador **MAPICRASH_RECOVER** , chamar **MAPICrashRecovery** com o **MAPICRASH\_continuar** sinalizador para permitir depuração continuar. 
    
   - **MAPICRASH\_SYSTEM_SHUTDOWN**: se o PSTs ou OSTs estiverem em um estado consistente, mover os dados em disco e bloquear o PSTs ou OSTs para impedir o acesso de leitura ou gravação. O PSTs ou OSTs não podem ser desbloqueados usando **MAPICRASH\_continuar**. Deve ser usado em combinação com **MAPICRASH\_recuperar**. 
    
## <a name="remarks"></a>Comentários

O byte superior (0xFF000000) é reservado para sinalizadores de recuperação de travamento específico do provedor.
  
Chamar **MAPICrashRecovery** com o **MAPICRASH\_recuperar** e os sinalizadores **MAPICRASH_SYSTEM_SHUTDOWN** em resposta à mensagem **WM_ENDSESSION** . 
  
## <a name="see-also"></a>Confira também

- [Sobre a API de recuperação de falhas MAPI](about-the-mapi-crash-recovery-api.md)
- [Usar a API de recuperação de falhas MAPI](how-to-use-the-mapi-crash-recovery-api.md)

