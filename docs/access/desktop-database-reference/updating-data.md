---
title: Atualizando dados (referência de banco de dados da área de trabalho do Access)
TOCTitle: Updating Data
ms:assetid: 02e82066-77c8-cbb2-db28-98e2fc94404c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248794(v=office.15)
ms:contentKeyID: 48542970
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8e6989468e23fc1c9c611eb091172822a6ffe938
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/18/2019
ms.locfileid: "28726334"
---
# <a name="updating-data"></a>Atualização de dados


**Aplica-se a**: Access 2013, o Office 2013

A atualização do comportamento e do recurso depende amplamente do modo Atualização (tipo de bloqueio), tipo de cursor e local do cursor.

Use o método **Update** para salvar quaisquer alterações feitas no registro atual de um objeto **Recordset** desde a chamada do método **AddNew** ou desde a alteração de quaisquer valores de campo em um registro existente. O objeto **Recordset** deve oferecer suporte às atualizações.

Se o objeto **Recordset** oferecer suporte à atualização do lote, você poderá armazenar em cache várias alterações em um ou mais registros localmente até que você chame o método **UpdateBatch**. Se você estiver editando o registro atual ou adicionando um novo registro ao chamar o método **UpdateBatch**, o ADO chamará automaticamente o método **Update** para salvar quaisquer alterações pendentes no registro atual antes de transmitir as alterações em lote para o provedor.

O registro atual permanece atual depois que você chama os métodos **Update** ou **UpdateBatch**.

Esta seção inclui os seguintes tópicos:

- [Modo Imediato](immediate-mode.md)
- [Processamento de transações](transaction-processing.md)
- [Modo de lotes (ADO)](batch-mode.md)

