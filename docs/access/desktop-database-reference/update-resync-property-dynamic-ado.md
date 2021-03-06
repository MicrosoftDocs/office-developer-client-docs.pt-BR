---
title: Propriedade dinâmica Update Resync (ADO)
TOCTitle: Update Resync dynamic property (ADO)
ms:assetid: 0af9cfd2-8042-65c9-cec6-77d2e7a88ad9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248842(v=office.15)
ms:contentKeyID: 48543166
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 653291ade258d602d7ec523dcac7e9fe51dd91fb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308341"
---
# <a name="update-resync-dynamic-property-ado"></a>Propriedade dinâmica Update Resync (ADO)


**Aplica-se ao:** Access 2013, Office 2013

Especifica se o método [UpdateBatch](updatebatch-method-ado.md) é seguido por uma operação de método [Resync](resync-method-ado.md) implícita e, em caso positivo, o escopo dessa operação.

## <a name="settings-and-return-values"></a>Configurações e valores de retorno

Define ou retorna um ou mais dos valores [ENUM ADCPROP \_ UPDATERESYNC. \_ ](adcprop-updateresync-enum.md)

## <a name="remarks"></a>Comentários

Os valores de ENUM ADCPROP UPDATERESYNC podem ser combinados, exceto \_ adResyncAll, que já representa a combinação do restante \_ dos valores.

A constante **adResyncConflicts** armazena os valores de ressincronização como valores de base, mas não substitui as alterações pendentes.

**Update Resync** é uma propriedade dinâmica acrescentada à coleção [Properties](recordset-object-ado.md) do objeto [Recordset](properties-collection-ado.md) quando a propriedade [CursorLocation](cursorlocation-property-ado.md) for configurada como **adUseClient**.

