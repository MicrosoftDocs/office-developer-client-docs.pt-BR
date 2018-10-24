---
title: Sobre a API de recuperação de falhas MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: bc1e1f55-1959-a4a9-a24d-f006af531c9a
description: 'Última modificação: 25 de julho de 2012'
ms.openlocfilehash: fbb6d22414daf3464e80fbf1d9cf92ccb3d560e3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576586"
---
# <a name="about-the-mapi-crash-recovery-api"></a>Sobre a API de recuperação de falhas MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
A API de recuperação MAPI travar verifica que o estado do arquivo de pastas particulares (. PST) ou o arquivo de pastas Offline (OST) compartilhado de memória para verificar se os dados estão em um estado consistente. Se ele estiver em um estado consistente, a função [MAPICrashRecovery](mapicrashrecovery.md) move os dados do open PSTs ou OSTs em disco e bloqueia o PSTs ou OSTs e não permitir que qualquer acesso de leitura ou gravação aos dados. Isso garante que os dados permaneçam em um estado consistente, até que o processo é encerrado. Garantindo que o PSTs ou OSTs estão em um estado consistente antes do processo é encerrado, você pode impedir que o Microsoft Outlook 2013 e o Microsoft Outlook 2010 exiba a seguinte mensagem de erro e evitar problemas de desempenho. 
  
 **Um arquivo de dados não foi fechado corretamente a última vez que foi usada e está sendo verificada para problemas. Desempenho poderá ser afetado enquanto a seleção estiver em andamento.**
  
Essa API oferece os seguintes recursos:
  
Constantes:
  
- [Constantes de MAPI](mapi-constants.md)
    
Funções:
  
- [MAPICrashRecovery](mapicrashrecovery.md)
    
## <a name="see-also"></a>Confira também



[Usar a API de recuperação de falhas MAPI](how-to-use-the-mapi-crash-recovery-api.md)

