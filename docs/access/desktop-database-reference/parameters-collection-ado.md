---
title: Coleção paraMeters (ADO)
TOCTitle: Parameters collection (ADO)
ms:assetid: 554387c3-3572-5391-3b24-c7d3443844cd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249283(v=office.15)
ms:contentKeyID: 48544923
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231103
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: feb24e0f498e02bae01ef689a2ad62e487e314bc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287941"
---
# <a name="parameters-collection-ado"></a>Coleção paraMeters (ADO)


**Aplica-se ao:** Access 2013, Office 2013

Contém todos os objetos [Parameter](parameter-object-ado.md) de um objeto [Command](command-object-ado.md).

## <a name="remarks"></a>Comentários

Um objeto **Command** tem uma coleção **Parameters** composta de objetos **Parameter**.

O uso do método [Refresh](refresh-method-ado.md) em uma coleção **Parameters** do objeto **Command** recupera as informações de parâmetro do provedor para o procedimento armazenado ou a consulta parametrizada especificada no objeto **Command**. Alguns provedores não oferecem suporte às chamadas de procedimento armazenadas ou às consultas parametrizadas; a chamada do método **Refresh** na coleção **Parameters** durante o uso desse provedor retornará um erro.

Se você não definiu seus próprios objetos **Parameter** e acessou a coleção **Parameters** antes de chamar o método **Refresh**, o ADO chamará automaticamente o método e preencherá a coleção.

Você pode minimizar as chamadas do provedor para melhorar o desempenho, se conhecer as propriedades dos parâmetros associadas ao procedimento armazenado ou à consulta parametrizada que quiser chamar. Use o método [CreateParameter](createparameter-method-ado.md) para criar objetos **Parameter** com as definições de propriedade adequadas e utilize o método [Append](append-method-ado.md) para adicioná-las à coleção **Parameters**. Isso permite definir e retornar os valores de parâmetro sem ter de chamar o provedor para obter as informações do parâmetro. Se você estiver gravando para um provedor que não forneça as informações de parâmetro, deverá preencher manualmente a coleção **Parameters** por meio desse método para usar os parâmetros totalmente. Use o método [Delete](delete-method-ado-parameters-collection.md) para remover os objetos **Parameter** da coleção **Parameters**, se necessário.

Os objetos da coleção **Parameters** de um **Recordset** sairão do escopo (e, por esse motivo, se tornarão não disponíveis), quando **Recordset** for fechado.

