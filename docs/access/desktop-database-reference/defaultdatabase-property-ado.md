---
title: Propriedade defaultDatabase (ADO)
TOCTitle: DefaultDatabase property (ADO)
ms:assetid: a35c5631-f9d9-e51f-950b-e52169830d94
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249757(v=office.15)
ms:contentKeyID: 48546784
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 01ca42ff738afe3a35cab6263cdae32ac256f3d1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294145"
---
# <a name="defaultdatabase-property-ado"></a>Propriedade defaultDatabase (ADO)


**Aplica-se ao:** Access 2013, Office 2013

Indica o banco de dados padrão para um objeto [Connection](connection-object-ado.md).

## <a name="settings-and-return-values"></a>Configurações e valores de retorno

Define ou retorna um valor **String** que avalia o nome de um banco de dados disponível no provedor.

## <a name="remarks"></a>Comentários

Use a propriedade **DefaultDatabase** para definir ou retornar o nome do banco de dados padrão em um objeto **Connection** específico.

Se houver um banco de dados padrão, as sequências SQL poderão usar uma sintaxe não qualificada para acessar objetos no banco de dados. Para acessar objetos em um banco de dados que não seja aquele especificado na propriedade **DefaultDatabase**, é preciso qualificar os nomes dos objetos com o nome do banco de dados desejado. Na conexão, o provedor gravará as informações do banco de dados padrão na propriedade **DefaultDatabase**. Alguns provedores permitem apenas um banco de dados por conexão, caso em que não é possível alterar a propriedade **DefaultDatabase**.

Algumas fontes de dados e provedores talvez não ofereçam suporte a esse recurso e podem retornar um erro ou uma cadeia de caracteres vazia.

**Uso do Remote Data Service** Esta propriedade não está disponível em um objeto **Connection** do lado do cliente.

