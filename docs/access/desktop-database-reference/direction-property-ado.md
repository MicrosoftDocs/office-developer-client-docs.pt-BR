---
title: Propriedade Direction (ADO)
TOCTitle: Direction property (ADO)
ms:assetid: 51a94abb-7ce9-9adb-2b76-5391eb9f6863
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249262(v=office.15)
ms:contentKeyID: 48544823
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5885e89a3bce5d8b16ea855ce14689380655ad45
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293865"
---
# <a name="direction-property-ado"></a>Propriedade Direction (ADO)


**Aplica-se ao:** Access 2013, Office 2013

Indica se o [Parameter](parameter-object-ado.md) representa um parâmetro de entrada, um parâmetro de saída, um parâmetro de entrada e saída ou se o parâmetro é o valor de retorno de um procedimento armazenado.

## <a name="settings-and-return-values"></a>Configurações e valores de retorno

Define ou retorna um valor [ParameterDirectionEnum](parameterdirectionenum.md).

## <a name="remarks"></a>Comentários

Use a propriedade **Direction** para especificar como um parâmetro é passado de ou para um procedimento. A propriedade **Direction** é leitura/gravação; isso permite trabalhar com provedores que não retornam essa informação ou definir essa informação quando não se deseja mais que o ADO faça uma chamada extra para o provedor a fim de recuperar informações de parâmetro.

Nem todos os provedores podem determinar a direção dos parâmetros em seus procedimentos armazenados. Nesses casos, você deve definir a propriedade **Direction** antes de executar a consulta.

