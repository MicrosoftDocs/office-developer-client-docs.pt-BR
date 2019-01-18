---
title: Tratamento de erros em Visual C++
TOCTitle: Handling errors in Visual C++
ms:assetid: 75e15699-0c84-1dca-654e-f9ac465c2a30
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249483(v=office.15)
ms:contentKeyID: 48545684
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d0e76dc3cc9634a1531a34058bf7a1baf636c94c
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709471"
---
# <a name="handling-errors-in-visual-c"></a>Tratamento de erros em Visual C++


**Aplica-se a**: Access 2013, o Office 2013

Em COM, a maioria das operações retorna um código HRESULT que indica se uma função foi concluída com êxito. O \#a diretiva de importação gera um código de wrapper ao redor de cada propriedade ou método "raw" e verifica o HRESULT retornado. Se o HRESULT indica uma falha, o código de wrapper lança um erro COM chamando \_com\_problema\_errorex() com o HRESULT retornar código como um argumento. Os objetos de erro COM podem ser capturados em um bloco **try-catch**. (Para a mesma da eficiência, catch uma referência a um \_com\_objeto error.)

Lembre-se de que esses erros são do ADO, pois resultam da falha de operação desse aplicativo. Os erros retornados pelo provedor subjacente aparecem como objetos **Error** na coleção **Errors** do objeto **Connection**.

O \#a diretiva de importação somente cria rotinas de tratamento de erros para métodos e propriedades declaradas na ADO. dll. Contudo, você pode utilizar esse mesmo mecanismo de tratamento de erros criando sua própria função inline ou macro de verificação de erros. Para obter exemplos, consulte o tópico "Extensões do Visual C++".

