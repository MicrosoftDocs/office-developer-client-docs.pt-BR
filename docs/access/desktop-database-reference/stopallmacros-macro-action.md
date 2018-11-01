---
title: Ação da macro PararTodasMacros
TOCTitle: StopAllMacros Macro Action
ms:assetid: 6afbf906-03b8-6e68-bbc9-7a4b141cf1c5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195440(v=office.15)
ms:contentKeyID: 48545442
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm104968
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 4d9452bed9a301c82d32c0c0a0800eb7b29231b0
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870510"
---
# <a name="stopallmacros-macro-action"></a>Ação da macro PararTodasMacros


**Aplica-se a**: Access 2013, o Office 2013

Você pode usar a ação **PararTodasMacros** para interromper todas as macros em execução no momento.

## <a name="setting"></a>Configuração

A ação **PararTodasMacros** não tem argumentos.

## <a name="remarks"></a>Comentários

Esta ação geralmente é usada quando uma condição de erro torna necessário parar todas as macros. Você pode usar uma expressão condicional na linha de ação da macro, contendo essa ação. Quando a expressão for avaliada como **True** (– 1), o Microsoft Access para todas as macros.

Por exemplo, você pode ter uma macro que exiba uma caixa de mensagem como uma de muitas ações complexas, incluindo a execução de outras macros. Se o usuário clicar em **Cancelar** nessa caixa de mensagem, a ação **PararTodasMacros** poderá interromper todas as macros em execução.

Se uma macro tiver usado as ações **Eco** ou **DefinirAvisos** para desativar o eco ou a exibição de mensagens do sistema, a ação **PararTodasMacros** fará a reativação automaticamente.

Esta ação não está disponível em um módulo VBA (Visual Basic for Applications).

