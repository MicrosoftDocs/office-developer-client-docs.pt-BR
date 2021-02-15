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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292024"
---
# <a name="handling-errors-in-visual-c"></a>Tratamento de erros em Visual C++


**Aplica-se ao:** Access 2013, Office 2013

No COM, a maioria das operações retornam um código de retorno HRESULT que indica que uma função foi concluída com sucesso. A diretiva de importação gera código wrapper em torno de cada propriedade ou método \# "bruto" e verifica o HRESULT retornado. Se o HRESULT indicar falha, o código wrapper lançará um erro COM chamando com issue errorex() com o código de retorno \_ \_ \_ HRESULT como um argumento. Os objetos de erro COM podem ser capturados em um bloco **try-catch**. (Por uma questão de eficiência, captura uma referência a um \_ objeto de erro de \_ com.)

Lembre-se de que esses erros são do ADO, pois resultam da falha de operação desse aplicativo. Os erros retornados pelo provedor subjacente aparecem como objetos **Error** na coleção **Errors** do objeto **Connection**.

A diretiva de importação só cria rotinas de tratamento de erros para métodos e propriedades \# declarados no ADO .dll. Contudo, você pode utilizar esse mesmo mecanismo de tratamento de erros criando sua própria função inline ou macro de verificação de erros. Para obter exemplos, consulte o tópico "Extensões do Visual C++".

