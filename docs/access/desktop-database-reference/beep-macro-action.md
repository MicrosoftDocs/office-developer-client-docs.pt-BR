---
title: Ação da macro AlarmeSonoro (referência do banco de dados do Access)
TOCTitle: Beep macro action
ms:assetid: 5ca1600f-7934-3b3d-19fd-f305cda0e5d8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194572(v=office.15)
ms:contentKeyID: 48545092
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm11853
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 96051d8389f4b8ba7005c75ccdb5e2780ba17138
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296861"
---
# <a name="beep-macro-action"></a>Ação da macro AlarmeSonoro


**Aplica-se ao:** Access 2013, Office 2013

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

