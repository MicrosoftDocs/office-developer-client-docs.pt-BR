---
title: Propriedade Database.Connection (DAO)
TOCTitle: Connection Property
ms:assetid: 8b900ea4-9179-9ed1-bc0b-0576939bb2bd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197325(v=office.15)
ms:contentKeyID: 48546221
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d000d2f01bea7746fb249ab7f9acacc047029b21
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463059"
---
# <a name="databaseconnection-property-dao"></a>Propriedade Database.Connection (DAO)


**Aplica-se a**: Access 2013 | Office 2013

## <a name="syntax"></a>Sintaxe

*expressão* . Conexão

*expressão* Uma variável que representa um objeto de **banco de dados** .

## <a name="remarks"></a>Comentários

Use a propriedade **Connection** para obter uma referência a um objeto **Connection** que corresponda ao **Database**. No DAO, um objeto **Connection** e seus objetos **Database** correspondentes são simplesmente duas referências diferentes de variáveis de objeto para o mesmo objeto. A propriedade **[Database](connection-database-property-dao.md)** de um objeto **Connection** e a propriedade **Connection** de um objeto **Database** facilita a alteração das conexões para uma fonte de dados ODBC por meio do mecanismo de banco de dados do Microsoft Access a fim de usar o ODBCDirect.

