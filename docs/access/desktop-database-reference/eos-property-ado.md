---
title: Propriedade EOS (ADO - referência de banco de dados da área de trabalho do Access))
TOCTitle: EOS property (ADO)
ms:assetid: 97cd23ef-cca8-4dcc-2641-082a0e1b853c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249676(v=office.15)
ms:contentKeyID: 48546474
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 32b76259f9be90ebd60cbc8c618a4d2bb80de165
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870118"
---
# <a name="eos-property-ado"></a>Propriedade EOS (ADO)


**Aplica-se a**: Access 2013, o Office 2013

Indica se a posição atual está no final do fluxo.

## <a name="return-values"></a>Valor de retorno

Retorna um valor **Boolean** que indica se a posição atual está no final do fluxo. O **EOS** retorna **True** quando não há mais bytes no fluxo; e retorna **False** quando há mais bytes após a posição atual.

Para definir o final da posição do fluxo, use o método [SetEOS](seteos-method-ado.md). Para determinar a posição atual, use a propriedade [Position](position-property-ado.md).

