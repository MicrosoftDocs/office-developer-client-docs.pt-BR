---
title: Propriedade prompt dinâmica (ADO)
TOCTitle: Prompt dynamic property (ADO)
ms:assetid: 6c899b03-1d1f-a81f-dc17-7205a0230af9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249428(v=office.15)
ms:contentKeyID: 48545473
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1898169881042b9c7af36668e26c93200d0cb5f8
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25924614"
---
# <a name="prompt-dynamic-property-ado"></a><span data-ttu-id="a16dd-102">Propriedade prompt dinâmica (ADO)</span><span class="sxs-lookup"><span data-stu-id="a16dd-102">Prompt dynamic property (ADO)</span></span>


<span data-ttu-id="a16dd-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="a16dd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a16dd-104">Especifica se o provedor OLE DB deveria solicitar ao usuário as informações de inicialização.</span><span class="sxs-lookup"><span data-stu-id="a16dd-104">Specifies whether the OLE DB provider should prompt the user for initialization information.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="a16dd-105">Configurações e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="a16dd-105">Settings and return values</span></span>

<span data-ttu-id="a16dd-106">Define e retorna um valor [ConnectPromptEnum](connectpromptenum.md).</span><span class="sxs-lookup"><span data-stu-id="a16dd-106">Sets and returns a [ConnectPromptEnum](connectpromptenum.md) value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a16dd-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="a16dd-107">Remarks</span></span>

<span data-ttu-id="a16dd-p101">**Prompt** é uma propriedade dinâmica que pode ser acrescentada à coleção [Properties](connection-object-ado.md) do objeto [Connection](properties-collection-ado.md) pelo provedor OLE DB. Para solicitar informações de inicialização, normalmente, os provedores OLE DB exibem uma caixa de diálogo para o usuário.</span><span class="sxs-lookup"><span data-stu-id="a16dd-p101">**Prompt** is a dynamic property, which may be appended to the [Connection](connection-object-ado.md) object's [Properties](properties-collection-ado.md) collection by the OLE DB provider. To prompt for initialization information, OLE DB providers will typically display a dialog box to the user.</span></span>

<span data-ttu-id="a16dd-p102">As propriedades dinâmicas de um objeto [Connection](connection-object-ado.md) são perdidas quando **Connection** é fechado. A propriedade **Prompt** deve ser redefinida antes de reabrir o objeto **Connection** para usar um valor diferente do padrão.</span><span class="sxs-lookup"><span data-stu-id="a16dd-p102">Dynamic properties of a [Connection](connection-object-ado.md) object are lost when the **Connection** is closed. The **Prompt** property must be reset before re-opening the **Connection** to use a value other than the default.</span></span>


> [!NOTE]
> <P><span data-ttu-id="a16dd-p103">[!OBSERVAçãO] Não especifique que o provedor solicite o usuário em cenários nos quais este não será capaz de responder à caixa de diálogo. Por exemplo, o usuário não será capaz de responder se o aplicativo estiver sendo executado em um sistema de servidor, e não no cliente do usuário, ou se o aplicativo estiver sendo executado em um sistema em que não haja nenhum usuário conectado. Nesses casos, o aplicativo esperará indefinidamente por uma resposta e parecerá que está travado.</span><span class="sxs-lookup"><span data-stu-id="a16dd-p103">Do not specify that the provider should prompt the user in scenarios in which the user will not be able to respond to the dialog box. For example, the user will not be able to respond if the application is running on a server system instead of on the user's client, or if the application is running on a system with no user logged on. In these cases, the application will wait indefinitely for a response and seem to lock up.</span></span></P>



<span data-ttu-id="a16dd-115">**Uso**</span><span class="sxs-lookup"><span data-stu-id="a16dd-115">**Usage**</span></span>

```vb
    Set cn = New Connection
    cn.Provider = "SQLOLEDB"
    cn.Properties("Prompt") = adPromptNever    ' do not prompt the user
```
