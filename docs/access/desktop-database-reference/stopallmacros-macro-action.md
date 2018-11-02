---
title: Ação da macro PararTodasMacros
TOCTitle: StopAllMacros macro action
ms:assetid: 6afbf906-03b8-6e68-bbc9-7a4b141cf1c5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195440(v=office.15)
ms:contentKeyID: 48545442
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm104968
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 34dbfc3504744dd446a018e797ebacfb79066d96
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923347"
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

