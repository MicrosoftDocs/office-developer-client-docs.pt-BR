---
title: Ação de Macro AlarmeSonoro (referência de banco de dados da área de trabalho do Access)
TOCTitle: Beep Macro Action
ms:assetid: 5ca1600f-7934-3b3d-19fd-f305cda0e5d8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194572(v=office.15)
ms:contentKeyID: 48545092
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm11853
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 7024734b09544042fa58b8cd95127d8195e5788a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464761"
---
# <a name="beep-macro-action"></a>Ação de macro AlarmeSonoro


**Aplica-se a**: Access 2013 | Office 2013

Você pode usar a ação **AlarmeSonoro** para emitir um tom de alarme sonoro pelo alto-falante do computador.

## <a name="setting"></a>Configuração

A ação **AlarmeSonoro** não tem nenhum argumento.

## <a name="remarks"></a>Comentários

Você pode usar a ação **AlarmeSonoro** para sinalizar as seguintes ocorrências:

  - Importantes alterações de tela.

  - Foram inseridos tipos errados de dados em um controle. Por exemplo, o usuário inseriu dados numéricos em um controle de caixa de texto.

  - Uma macro atingiu um ponto especificado ou concluiu suas ações.

A frequência e a duração do alarme sonoro dependem do hardware, que pode variar entre computadores.

Para executar a ação **AlarmeSonoro** em um módulo do VBA (Visual Basic for Applications), use o método **Beep** do objeto **DoCmd**.

