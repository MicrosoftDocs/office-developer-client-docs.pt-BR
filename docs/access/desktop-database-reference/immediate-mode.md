---
title: Modo imediato (referência do banco de dados da área de trabalho do Access)
TOCTitle: Immediate mode
ms:assetid: 61bd3645-6e84-2e3a-7814-37d8c1247df0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249362(v=office.15)
ms:contentKeyID: 48545220
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3abc2e8365c60987fedc0d306b274df74c7ee551
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291877"
---
# <a name="immediate-mode"></a>Modo Imediato


**Aplica-se ao:** Access 2013, Office 2013

O modo imediato entra em vigor quando a propriedade **LockType** é definida como **adLockOptimistic** ou **adLockPessimistic**. Nesse modo, as alterações feitas em um registro são propagadas na fonte de dados logo que você declara concluído o trabalho em uma linha chamando o método **Update**.

## <a name="calling-update"></a>Chamando o método Update

Se você sair do registro que está adicionando ou editando, antes de chamar o método **Update**, o ADO chamará automaticamente o método **Update** para salvar as alterações. Você deverá chamar o método **CancelUpdate** antes da navegação se quiser cancelar as alterações feitas no registro atual ou descartar um registro recém-adicionado.

O registro atual permanecerá atual após a chamada do método **Update**.

## <a name="cancelupdate"></a>CancelUpdate

Use o método **CancelUpdate** para cancelar as alterações feitas na linha atual ou descartar uma linha recém-adicionada. Você não pode cancelar as alterações feitas na linha atual ou em uma nova linha após a chamada do método **Update**, a menos que as alterações façam parte de uma transação que você possa cancelar com o método **RollbackTrans** ou parte de uma atualização em lotes. No caso de uma atualização em lotes, é possível cancelar o método **Update** com o método **CancelUpdate** ou **CancelBatch**.

Se você estiver adicionando uma nova linha ao chamar o método **CancelUpdate**, a linha atual se tornará a linha que era atual antes da chamada de **AddNew**.

Se você não tiver alterado a linha atual nem adicionado uma nova linha, a chamada do método **CancelUpdate** gerará um erro.

