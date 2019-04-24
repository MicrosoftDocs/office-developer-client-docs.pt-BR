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

No COM, a maioria das operações retornam um código de retorno HRESULT que indica que uma função foi concluída com sucesso. A \#política de importação gera código de wrapper ao redor de cada método ou propriedade "RAW" e verifica o HRESULT retornado. Se o HRESULT indicar falha, o código de wrapper gerará um erro COM \_chamando\_o\_problema com errorex () com o código de retorno HRESULT como um argumento. Os objetos de erro COM podem ser capturados em um bloco **try-catch**. (Para fins de eficiência, Capture uma referência a um \_objeto\_Error com.)

Lembre-se de que esses erros são do ADO, pois resultam da falha de operação desse aplicativo. Os erros retornados pelo provedor subjacente aparecem como objetos **Error** na coleção **Errors** do objeto **Connection**.

A \#política de importação cria apenas rotinas de tratamento de erros para métodos e propriedades declaradas no ADO. dll. Contudo, você pode utilizar esse mesmo mecanismo de tratamento de erros criando sua própria função inline ou macro de verificação de erros. Para obter exemplos, consulte o tópico "Extensões do Visual C++".

