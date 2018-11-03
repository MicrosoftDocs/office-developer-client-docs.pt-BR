---
title: Tratando erros no Visual C++
TOCTitle: Handling errors in Visual C++
ms:assetid: 75e15699-0c84-1dca-654e-f9ac465c2a30
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249483(v=office.15)
ms:contentKeyID: 48545684
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 99f8a0f8c7b79769fba62b38ef5517781aea4600
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25945604"
---
# <a name="handling-errors-in-visual-c"></a><span data-ttu-id="cadc4-102">Tratando erros no Visual C++</span><span class="sxs-lookup"><span data-stu-id="cadc4-102">Handling errors in Visual C++</span></span>


<span data-ttu-id="cadc4-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="cadc4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cadc4-104">Em COM, a maioria das operações retorna um código HRESULT que indica se uma função foi concluída com êxito.</span><span class="sxs-lookup"><span data-stu-id="cadc4-104">In COM, most operations return an HRESULT return code that indicates whether a function completed successfully.</span></span> <span data-ttu-id="cadc4-105">O \#a diretiva de importação gera um código de wrapper ao redor de cada propriedade ou método "raw" e verifica o HRESULT retornado.</span><span class="sxs-lookup"><span data-stu-id="cadc4-105">The \#import directive generates wrapper code around each "raw" method or property and checks the returned HRESULT.</span></span> <span data-ttu-id="cadc4-106">Se o HRESULT indica uma falha, o código de wrapper lança um erro COM chamando \_com\_problema\_errorex() com o HRESULT retornar código como um argumento.</span><span class="sxs-lookup"><span data-stu-id="cadc4-106">If the HRESULT indicates failure, the wrapper code throws a COM error by calling \_com\_issue\_errorex() with the HRESULT return code as an argument.</span></span> <span data-ttu-id="cadc4-107">Os objetos de erro COM podem ser capturados em um bloco **try-catch**.</span><span class="sxs-lookup"><span data-stu-id="cadc4-107">COM error objects can be caught in a **try-catch** block.</span></span> <span data-ttu-id="cadc4-108">(Para a mesma da eficiência, catch uma referência a um \_com\_objeto error.)</span><span class="sxs-lookup"><span data-stu-id="cadc4-108">(For efficiency's sake, catch a reference to a \_com\_error object.)</span></span>

<span data-ttu-id="cadc4-p102">Lembre-se de que esses erros são do ADO, pois resultam da falha de operação desse aplicativo. Os erros retornados pelo provedor subjacente aparecem como objetos **Error** na coleção **Errors** do objeto **Connection**.</span><span class="sxs-lookup"><span data-stu-id="cadc4-p102">Remember, these are ADO errors: they result from the ADO operation failing. Errors returned by the underlying provider appear as **Error** objects in the **Connection** object's **Errors** collection.</span></span>

<span data-ttu-id="cadc4-111">O \#a diretiva de importação somente cria rotinas de tratamento de erros para métodos e propriedades declaradas na ADO. dll.</span><span class="sxs-lookup"><span data-stu-id="cadc4-111">The \#import directive only creates error-handling routines for methods and properties declared in the ADO .dll.</span></span> <span data-ttu-id="cadc4-112">Contudo, você pode utilizar esse mesmo mecanismo de tratamento de erros criando sua própria função inline ou macro de verificação de erros.</span><span class="sxs-lookup"><span data-stu-id="cadc4-112">However, you can take advantage of this same error-handling mechanism by writing your own error-checking macro or inline function.</span></span> <span data-ttu-id="cadc4-113">Para obter exemplos, consulte o tópico "Extensões do Visual C++".</span><span class="sxs-lookup"><span data-stu-id="cadc4-113">See the topic Visual C++ Extensions for examples.</span></span>

