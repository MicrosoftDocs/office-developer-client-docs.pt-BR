---
title: Propriedade EOS (ADO - referência de banco de dados da área de trabalho do Access))
TOCTitle: EOS property (ADO)
ms:assetid: 97cd23ef-cca8-4dcc-2641-082a0e1b853c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249676(v=office.15)
ms:contentKeyID: 48546474
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a35503fb0ad320e82ed385c7014b2a18de586064
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716597"
---
# <a name="eos-property-ado"></a><span data-ttu-id="1b846-102">Propriedade EOS (ADO)</span><span class="sxs-lookup"><span data-stu-id="1b846-102">EOS property (ADO)</span></span>


<span data-ttu-id="1b846-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="1b846-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1b846-104">Indica se a posição atual está no final do fluxo.</span><span class="sxs-lookup"><span data-stu-id="1b846-104">Indicates whether the current position is at the end of the stream.</span></span>

## <a name="return-values"></a><span data-ttu-id="1b846-105">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="1b846-105">Return values</span></span>

<span data-ttu-id="1b846-p101">Retorna um valor **Boolean** que indica se a posição atual está no final do fluxo. O **EOS** retorna **True** quando não há mais bytes no fluxo; e retorna **False** quando há mais bytes após a posição atual.</span><span class="sxs-lookup"><span data-stu-id="1b846-p101">Returns a **Boolean** value that indicates whether the current position is at the end of the stream. **EOS** returns **True** if there are no more bytes in the stream; it returns **False** if there are more bytes following the current position.</span></span>

<span data-ttu-id="1b846-p102">Para definir o final da posição do fluxo, use o método [SetEOS](seteos-method-ado.md). Para determinar a posição atual, use a propriedade [Position](position-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="1b846-p102">To set the end of stream position, use the [SetEOS](seteos-method-ado.md) method. To determine the current position, use the [Position](position-property-ado.md) property.</span></span>

