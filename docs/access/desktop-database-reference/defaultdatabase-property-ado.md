---
title: Propriedade DefaultDatabase (ADO)
TOCTitle: DefaultDatabase property (ADO)
ms:assetid: a35c5631-f9d9-e51f-950b-e52169830d94
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249757(v=office.15)
ms:contentKeyID: 48546784
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6238192f123e31c27a0e553d548be0b1623f0a32
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882326"
---
# <a name="defaultdatabase-property-ado"></a>Propriedade DefaultDatabase (ADO)


**Aplica-se a**: Access 2013, o Office 2013

Indica o banco de dados padrão para um objeto [Connection](connection-object-ado.md).

## <a name="settings-and-return-values"></a>Configurações e valores de retorno

Define ou retorna um valor **String** que avalia o nome de um banco de dados disponível no provedor.

## <a name="remarks"></a>Comentários

Use a propriedade **DefaultDatabase** para definir ou retornar o nome do banco de dados padrão em um objeto **Connection** específico.

Se houver um banco de dados padrão, as sequências SQL poderão usar uma sintaxe não qualificada para acessar objetos no banco de dados. Para acessar objetos em um banco de dados que não seja aquele especificado na propriedade **DefaultDatabase**, é preciso qualificar os nomes dos objetos com o nome do banco de dados desejado. Na conexão, o provedor gravará as informações do banco de dados padrão na propriedade **DefaultDatabase**. Alguns provedores permitem apenas um banco de dados por conexão, caso em que não é possível alterar a propriedade **DefaultDatabase**.

Algumas fontes de dados e provedores talvez não ofereçam suporte a esse recurso e podem retornar um erro ou uma cadeia de caracteres vazia.

**Uso de serviço de dados remotos** Essa propriedade não está disponível em um objeto de **Conexão** do cliente.

