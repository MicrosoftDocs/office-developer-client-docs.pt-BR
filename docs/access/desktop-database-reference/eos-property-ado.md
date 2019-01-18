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
# <a name="eos-property-ado"></a>Propriedade EOS (ADO)


**Aplica-se a**: Access 2013, o Office 2013

Indica se a posição atual está no final do fluxo.

## <a name="return-values"></a>Valores de retorno

Retorna um valor **Boolean** que indica se a posição atual está no final do fluxo. O **EOS** retorna **True** quando não há mais bytes no fluxo; e retorna **False** quando há mais bytes após a posição atual.

Para definir o final da posição do fluxo, use o método [SetEOS](seteos-method-ado.md). Para determinar a posição atual, use a propriedade [Position](position-property-ado.md).

