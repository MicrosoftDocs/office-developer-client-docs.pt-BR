---
title: Sobre a API de recuperação de falhas MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: bc1e1f55-1959-a4a9-a24d-f006af531c9a
description: '�ltima altera��o: segunda-feira, 25 de junho de 2012'
ms.openlocfilehash: 1acca6d806c1734007ac7c5e41059d3a870dc5bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420259"
---
# <a name="about-the-mapi-crash-recovery-api"></a>Sobre a API de recuperação de falhas MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
A API de Recuperação de Falhas MAPI verifica o estado da memória compartilhada do arquivo de Pastas Particulares (PST) ou do arquivo de Pastas Offline (OST) para verificar se os dados estão em um estado consistente. Se estiver em um estado consistente, a função [MAPICrashRecovery](mapicrashrecovery.md) move os dados de PSTs ou OSTs abertos para o disco e bloqueia os PSTs ou OSTs e não permite acesso de leitura ou gravação aos dados. Isso garante que os dados permaneçam em um estado consistente até que o processo seja encerrado. Ao garantir que os PSTs ou OSTs estão em um estado consistente antes de o processo ser encerrado, você pode impedir que o Microsoft Outlook 2013 e o Microsoft Outlook 2010 exibem a seguinte mensagem de erro e evitar problemas de desempenho. 
  
 **Um arquivo de dados não foi fechado corretamente na última vez em que foi usado e está sendo verificado em busca de problemas. O desempenho pode ser afetado enquanto a verificação está em andamento.**
  
Essa API fornece o seguinte:
  
Constantes:
  
- [Constantes MAPI](mapi-constants.md)
    
Funções:
  
- [MAPICrashRecovery](mapicrashrecovery.md)
    
## <a name="see-also"></a>Confira também



[Usar a API de recuperação de falhas MAPI](how-to-use-the-mapi-crash-recovery-api.md)

