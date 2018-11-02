---
title: Ação da macro TransferirBancoDeDadosSQL
TOCTitle: TransferSQLDatabase macro action
ms:assetid: 8cb95e22-f1f0-6c70-7dcb-3a3e9aafdc57
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197344(v=office.15)
ms:contentKeyID: 48546244
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm111536
f1_categories:
- Office.Version=v15
ms.openlocfilehash: ae05da3d07cc17f54584d11282721ac83f23ccd8
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926539"
---
# <a name="transfersqldatabase-macro-action"></a>Ação da macro TransferirBancoDeDadosSQL


**Aplica-se a**: Access 2013, o Office 2013

Em um projeto do Access, você pode usar a ação **TransferirBancoDeDadosSQL** para transferir um banco de dados do Microsoft SQL Server 7.0 ou posterior para outro banco de dados SQL Server 7.0 ou posterior. Para obter mais informações sobre como transferir um banco de dados, consulte a documentação do SQL Server.


> [!NOTE]
> [!OBSERVAçãO] This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.



## <a name="setting"></a>Configuração

A ação **TransferirBancoDeDadosSQL** tem os seguintes argumentos.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argumento da ação</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Server</strong></p></td>
<td><p>O nome do servidor de banco de dados do SQL Server 7.0 ou posterior no qual você está copiando.</p></td>
</tr>
<tr class="even">
<td><p><strong>Database</strong></p></td>
<td><p>O nome do novo banco de dados a ser criado no servidor de destino.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Usar conexão confiável</strong></p></td>
<td><p>Especifica se há ou não é uma conexão confiável ao SQL Server. Se definido como <strong>Sim</strong>, não há uma conexão confiável e os argumentos de <strong>logon</strong> e <strong>senha</strong> não são necessários. Se definido como <strong>não</strong>, o <strong>logon</strong> e a <strong>senha</strong> de argumentos é necessário. O padrão é <strong>Sim</strong>. Quando você usa uma conexão confiável, a segurança do SQL Server se integra com a segurança do sistema operacional Windows para fornecer um logon único com a rede e o banco de dados.</p></td>
</tr>
<tr class="even">
<td><p><strong>Logon</strong></p></td>
<td><p>O nome do logon no servidor de destino.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Password</strong></p></td>
<td><p>A senha do argumento <strong>Logon</strong>. Essa senha é armazenada como texto no projeto do Access, mas fica oculta durante a operação de transferência de banco de dados.</p></td>
</tr>
<tr class="even">
<td><p><strong>Transferir dados de cópia</strong></p></td>
<td><p>Especifica se os dados devem ser incluídos na operação de transferência de banco de dados. Se definido como <strong>Sim</strong>, todos os dados serão incluídos em todas as tabelas, juntamente com todas as estruturas de dados, propriedades estendidas e objetos de banco de dados. Se definido como <strong>Não</strong>, nenhum dado será incluído nas tabelas. Somente a estrutura da tabela e as propriedades estendidas serão criadas no servidor de destino, juntamente com todos os outros objetos de banco de dados (com exceção dos diagramas de banco de dados). O padrão é <strong>Sim</strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

Não é possível executar outras operações enquanto o banco de dados está sendo transferido.

A ação **TransferirBancoDeDadosSQL**, por padrão, copia dados, definições de dados, objetos de banco de dados e propriedades estendidas; por exemplo, valores padrão, restrições de texto e valores de pesquisa.

Há requisitos para a transferência de um banco de dados:

  - Você deve ser membro da função sysadmin no servidor de destino (nenhuma função especial é exigida no servidor de origem).

<!-- end list -->

  - O servidor SQL atualmente conectado ao projeto do Access e ao servidor de destino para o qual você está transferindo o banco de dados deve ser SQL Server versão 7.0 ou posterior.


> [!NOTE]
> <P>[!OBSERVAçãO] Servidores vinculados não são transferidos durante a operação de transferência de banco de dados.</P>



Para executar a ação **TransferirBancoDeDadosSQL** em um módulo do VBA (Visual Basic for Applications), use o método **TransferSQLDatabase** do objeto **DoCmd**.

