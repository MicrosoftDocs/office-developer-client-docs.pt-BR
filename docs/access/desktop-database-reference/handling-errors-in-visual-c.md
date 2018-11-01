---
title: Tratando erros no Visual C++
TOCTitle: Handling Errors in Visual C++
ms:assetid: 75e15699-0c84-1dca-654e-f9ac465c2a30
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249483(v=office.15)
ms:contentKeyID: 48545684
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 937454a9277ec219f25a79074833138f6dd7f535
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887564"
---
# <a name="handling-errors-in-visual-c"></a>Tratando erros no Visual C++


**Aplica-se a**: Access 2013, o Office 2013

Em COM, a maioria das operações retorna um código HRESULT que indica se uma função foi concluída com êxito. O \#a diretiva de importação gera um código de wrapper ao redor de cada propriedade ou método "raw" e verifica o HRESULT retornado. Se o HRESULT indica uma falha, o código de wrapper lança um erro COM chamando \_com\_problema\_errorex() com o HRESULT retornar código como um argumento. Os objetos de erro COM podem ser capturados em um bloco **try-catch**. (Para a mesma da eficiência, catch uma referência a um \_com\_objeto error.)

Lembre-se de que esses erros são do ADO, pois resultam da falha de operação desse aplicativo. Os erros retornados pelo provedor subjacente aparecem como objetos **Error** na coleção **Errors** do objeto **Connection**.

O \#a diretiva de importação somente cria rotinas de tratamento de erros para métodos e propriedades declaradas na ADO. dll. Contudo, você pode utilizar esse mesmo mecanismo de tratamento de erros criando sua própria função inline ou macro de verificação de erros. Para obter exemplos, consulte o tópico "Extensões do Visual C++".

