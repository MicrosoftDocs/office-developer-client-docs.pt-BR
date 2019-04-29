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
  
A função **MAPICrashRecovery** verifica o estado do arquivo de pastas particulares (PST) ou da memória compartilhada do arquivo de pastas offline (OST). Se a memória estiver em um estado consistente, a função **MAPICrashRecovery** moverá os dados para o disco e impedirá o acesso de leitura ou gravação adicional até que o processo seja encerrado. 
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Exportado por:  <br/> |olmapi32. dll  <br/> |
|Chamado por:  <br/> |Cliente  <br/> |
|Implementado por:  <br/> |Outlook  <br/> |
   
```cpp
void MAPICrashRecovery(ULONG ulFlags);
```

## <a name="parameters"></a>Parâmetros

_ulFlags_
  
> no Sinalizadores usados para controlar como a recuperação de falha MAPI é executada. Os seguintes sinalizadores podem ser definidos:
    
   - **Recuperação\_de MAPICRASH**: se o PSTs ou o OSTs estiverem em um estado consistente, mova os dados para o disco e bloqueie os PSTs ou OSTs para evitar acesso de leitura ou gravação.
    
   - **MAPICRASH\_continuar**: Desbloqueie os PSTs ou OSTs para depuração. Após uma chamada bem-sucedida para **MAPICrashRecovery** com o sinalizador **MAPICRASH_RECOVER** , chame **MAPICrashRecovery** com o **sinalizador\_MAPICRASH continue** para permitir a depuração continuar. 
    
   - **MAPICRASH\_SYSTEM_SHUTDOWN**: se o PSTs ou o OSTs estiverem em um estado consistente, mova os dados para o disco e bloqueie o PSTs ou OSTs para impedir o acesso de leitura ou gravação. PSTs ou OSTs não podem ser desbloqueados usando o **MAPICRASH\_continue**. Deve ser usado em combinação com **a\_recuperação do MAPICRASH**. 
    
## <a name="remarks"></a>Comentários

O byte superior (0xFF000000) é reservado para sinalizadores de recuperação de pane específicos do provedor.
  
Chame **MAPICrashRecovery** com os **sinalizadores\_MAPICRASH Recover** e **MAPICRASH_SYSTEM_SHUTDOWN** em resposta à mensagem **WM_ENDSESSION** . 
  
## <a name="see-also"></a>Confira também

- [Sobre a API de recuperação de falhas MAPI](about-the-mapi-crash-recovery-api.md)
- [Usar a API de recuperação de falhas MAPI](how-to-use-the-mapi-crash-recovery-api.md)

