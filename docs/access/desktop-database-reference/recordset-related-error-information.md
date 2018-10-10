---
title: Informações sobre erros relacionados a recordsets
TOCTitle: Recordset-Related Error Information
ms:assetid: 388308c7-e121-bd12-228a-312c897b8c55
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249136(v=office.15)
ms:contentKeyID: 48544222
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 62f9a6d235b6c06ad8e7fa49d7b89960fd1ad2b5
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464269"
---
# <a name="recordset-related-error-information"></a>Informações sobre erros relacionados a recordsets


**Aplica-se a**: Access 2013 | Office 2013

Durante o processamento em lote, a propriedade **Status** do objeto **Recordset** fornece informações sobre os registros individuais no **Recordset**. Antes de ocorrer uma atualização em lote, a propriedade **Status** do **Recordset** reflete informações sobre os registros a serem adicionados, alterados e excluídos. 

Depois que **UpdateBatch** tiver sido chamado, a propriedade **Status** indicará o êxito ou a falha da operação. Conforme você se move de registro em registro no **Recordset,** o valor da propriedade **Status** é alterado para descrever o status do registro atual.

