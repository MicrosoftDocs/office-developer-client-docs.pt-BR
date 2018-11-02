---
title: Objeto de Conexão (DAO)
TOCTitle: Connection Object
ms:assetid: f469b04e-2539-6b53-31f2-85fe22fcc2fc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836694(v=office.15)
ms:contentKeyID: 48548690
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0473a3f4b920e05ad07556b070ed0e778d7ac694
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25930151"
---
# <a name="connection-object-dao"></a>Objeto de Conexão (DAO)


**Aplica-se a**: Access 2013, o Office 2013

> [!NOTE]
> [!OBSERVAçãO] O Microsoft Access 2013 não oferece suporte para espaços de trabalho ODBCDirect. Use ADO para acessar fontes de dados externas sem usar o mecanismo de banco de dados do Microsoft Access.



Um objeto **Connection** representa uma conexão com um banco de dados ODBC (apenas espaços de trabalho ODBCDirect).

## <a name="remarks"></a>Comentários

**Connection** é um objeto não persistente que representa uma conexão com um banco de dados remoto. O objeto **Connection** está disponível somente nos espaços de trabalho ODBCDirect (isto é, um objeto **Workspace** criado com a opção de tipo definida como **dbUseODBC**).


> [!NOTE]
> [!OBSERVAçãO] O código gravado por versões anteriores do DAO pode continuar usando o objeto **Database** para obter compatibilidade com versões anteriores, mas se os novos recursos de um objeto **Connection** forem desejados, você deverá revisar o código para usar o objeto **Connection**. Para ajudar na conversão de código, será possível obter uma referência do objeto **Connection** a partir de um **Database**, lendo a propriedade [Connection](database-connection-property-dao.md) do objeto **Database**. Por outro lado, você pode obter uma referência do objeto **Database** a partir da propriedade **Database** do objeto **Connection**.


