---
title: Propriedade Workspace.IsolateODBCTrans (DAO)
TOCTitle: IsolateODBCTrans Property
ms:assetid: f7a48358-870b-cad3-d4ef-e46b50428e12
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836924(v=office.15)
ms:contentKeyID: 48548770
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053083
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 197bf35c796fe1e34122b7d4214043e9217fb3d9
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25878539"
---
# <a name="workspaceisolateodbctrans-property-dao"></a>Propriedade Workspace.IsolateODBCTrans (DAO)


**Aplica-se a**: Access 2013, o Office 2013

Define ou retorna um valor que indica se vários transactiond, que envolvem o mesmo mecanismo do banco de dados do Microsoft Access conectado à fonte de dados ODBC, estão isolados (somente em espaços de trabalho do Microsoft Access).

## <a name="syntax"></a>Sintaxe

*expressão* . IsolateODBCTrans

*expressão* Uma variável que representa um objeto **Workspace** .

## <a name="remarks"></a>Comentários

Em algumas situações, será necessário ter várias transações simultâneas pendentes na mesma conexão ODBC. Para fazer isso, será necessário abrir um **Workspace** separado para cada transação. Embora cada **Workspace** possa ter sua própria conexão ODBC com o banco de dados, isso reduz a velocidade de desempenho do sistema. Como o isolamento da transação geralmente não é necessário, as conexões ODBC de vários objetos **Workspace** abertas pelo mesmo usuário são compartilhados por padrão.

Alguns servidores ODBC, como o Microsoft SQL Server, não permitem transações simultâneas em uma única conexão. Se você precisa ter mais de uma transação pendente simultânea em relação a um banco de dados, defina a propriedade **IsolateODBCTrans** como **True** em cada **Workspace** assim que abri-lo. Isso força uma conexão ODBC separada para cada **Workspace**.

