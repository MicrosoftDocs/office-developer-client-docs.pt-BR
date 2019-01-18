---
title: Informações de erro relacionado ao conjunto de registros
TOCTitle: Recordset-related error information
ms:assetid: 388308c7-e121-bd12-228a-312c897b8c55
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249136(v=office.15)
ms:contentKeyID: 48544222
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 12a67657d5543aac22a49690256b0410a2b901bd
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708897"
---
# <a name="recordset-related-error-information"></a>Informações de erro relacionado ao conjunto de registros

**Aplica-se a**: Access 2013, o Office 2013

Durante o processamento em lote, a propriedade **Status** do objeto **Recordset** fornece informações sobre os registros individuais no **Recordset**. Antes de ocorrer uma atualização em lote, a propriedade **Status** do **Recordset** reflete informações sobre os registros a serem adicionados, alterados e excluídos. 

Depois que **UpdateBatch** tiver sido chamado, a propriedade **Status** indicará o êxito ou a falha da operação. Conforme você se move de registro em registro no **Recordset,** o valor da propriedade **Status** é alterado para descrever o status do registro atual.

