---
title: Propriedade EOS (ADO - referência de banco de dados da área de trabalho do Access))
TOCTitle: EOS Property (ADO)
ms:assetid: 97cd23ef-cca8-4dcc-2641-082a0e1b853c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249676(v=office.15)
ms:contentKeyID: 48546474
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d4c6d96e2c143cb0548a2de987f11ea708d1669a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463577"
---
# <a name="eos-property-ado"></a>Propriedade EOS (ADO)


**Aplica-se a**: Access 2013 | Office 2013

Indica se a posição atual está no final do fluxo.

## <a name="return-values"></a>Valores de retorno

Retorna um valor **Boolean** que indica se a posição atual está no final do fluxo. O **EOS** retorna **True** quando não há mais bytes no fluxo; e retorna **False** quando há mais bytes após a posição atual.

Para definir o final da posição do fluxo, use o método [SetEOS](seteos-method-ado.md). Para determinar a posição atual, use a propriedade [Position](position-property-ado.md).

