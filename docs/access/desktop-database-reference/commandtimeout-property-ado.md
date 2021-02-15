---
title: Propriedade CommandTimeout (ADO)
TOCTitle: CommandTimeout property (ADO)
ms:assetid: a0b6209c-9feb-08ae-002a-15d1d20734a8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249739(v=office.15)
ms:contentKeyID: 48546714
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231124
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 9d44bc8fae0143b183ef54120cdaaf91337f36f8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296126"
---
# <a name="commandtimeout-property-ado"></a><span data-ttu-id="55a98-102">Propriedade CommandTimeout (ADO)</span><span class="sxs-lookup"><span data-stu-id="55a98-102">CommandTimeout property (ADO)</span></span>


<span data-ttu-id="55a98-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="55a98-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="55a98-104">Indica quanto tempo esperar durante a execução de um comando antes de interromper a tentativa e gerar um erro.</span><span class="sxs-lookup"><span data-stu-id="55a98-104">Indicates how long to wait while executing a command before terminating the attempt and generating an error.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="55a98-105">Configurações e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="55a98-105">Settings and return values</span></span>

<span data-ttu-id="55a98-106">Define ou retorna um valor **Long** que indica, em segundos, quanto tempo esperar para que um comando seja executado.</span><span class="sxs-lookup"><span data-stu-id="55a98-106">Sets or returns a **Long** value that indicates, in seconds, how long to wait for a command to execute.</span></span> <span data-ttu-id="55a98-107">O padrão é 30.</span><span class="sxs-lookup"><span data-stu-id="55a98-107">Default is 30.</span></span>

## <a name="remarks"></a><span data-ttu-id="55a98-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="55a98-108">Remarks</span></span>

<span data-ttu-id="55a98-p102">Use a propriedade **CommandTimeout** em um objeto [Connection](connection-object-ado.md) ou [Command](command-object-ado.md) para permitir o cancelamento de uma chamada do método [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) devido a atrasos no tráfego da rede ou uso intenso do servidor. Se o intervalo definido na propriedade **CommandTimeout** terminar antes de o comando concluir a execução, um erro será gerado e o ADO cancelará o comando. Se você definir a propriedade como zero, o ADO aguardará indefinidamente até que a execução seja concluída. Verifique se o provedor e a fonte de dados na qual está escrevendo o código oferecem suporte à funcionalidade **CommandTimeout**.</span><span class="sxs-lookup"><span data-stu-id="55a98-p102">Use the **CommandTimeout** property on a [Connection](connection-object-ado.md) object or [Command](command-object-ado.md) object to allow the cancellation of an [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) method call, due to delays from network traffic or heavy server use. If the interval set in the **CommandTimeout** property elapses before the command completes execution, an error occurs and ADO cancels the command. If you set the property to zero, ADO will wait indefinitely until the execution is complete. Make sure the provider and data source to which you are writing code support the **CommandTimeout** functionality.</span></span>

<span data-ttu-id="55a98-113">A definição de **CommandTimeout** em um objeto **Connection** não afeta a definição de **CommandTimeout** em um objeto **Command** no mesmo objeto **Connection**; isto é, a propriedade **CommandTimeout** do objeto **Command** não herda o valor de **CommandTimeout** do objeto **Connection**.</span><span class="sxs-lookup"><span data-stu-id="55a98-113">The **CommandTimeout** setting on a **Connection** object has no effect on the **CommandTimeout** setting on a **Command** object on the same **Connection**; that is, the **Command** object's **CommandTimeout** property does not inherit the value of the **Connection** object's **CommandTimeout** value.</span></span>

<span data-ttu-id="55a98-114">Em um objeto **Connection**, a propriedade **CommandTimeout** continua sendo de leitura/gravação depois que **Connection** é aberto.</span><span class="sxs-lookup"><span data-stu-id="55a98-114">On a **Connection** object, the **CommandTimeout** property remains read/write after the **Connection** is opened.</span></span>

