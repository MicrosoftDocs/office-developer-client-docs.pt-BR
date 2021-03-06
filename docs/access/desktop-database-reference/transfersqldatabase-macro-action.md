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
localization_priority: Normal
ms.openlocfilehash: 5ed20555726d0a6f63f0e48fb154cedb411ef8cd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306843"
---
# <a name="transfersqldatabase-macro-action"></a>Ação da macro TransferirBancoDeDadosSQL

**Aplica-se ao:** Access 2013, Office 2013

Em um projeto do Access, você pode usar a ação **TransferirBancoDeDadosSQL** para transferir um banco de dados do Microsoft SQL Server 7.0 ou posterior para outro banco de dados SQL Server 7.0 ou posterior. Para obter mais informações sobre como transferir um banco de dados, consulte a documentação do SQL Server.

> [!NOTE]
> Essa ação não será permitida se o banco de dados não for confiável.

## <a name="setting"></a>Setting

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
<td><p><strong>Banco de dados</strong></p></td>
<td><p>O nome do novo banco de dados a ser criado no servidor de destino.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Usar conexão confiável</strong></p></td>
<td><p>Especifica se há ou não uma conexão confiável para o SQL Server. Se definido como <strong>Sim</strong>, isso indicará que há uma conexão confiável e os argumentos <strong>Logon</strong> e <strong>Senha</strong> não serão exigidos. Se definido como <strong>Não</strong>, os argumentos <strong>Logon</strong> e <strong>Senha</strong> serão exigidos. O padrão é <strong>Sim</strong>. Quando você usa uma conexão confiável, a segurança do SQL Server se integra à segurança do sistema operacional Windows para fornecer um único logoff na rede e no banco de dados.</p></td>
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

- O servidor SQL atualmente conectado ao projeto do Access e ao servidor de destino para o qual você está transferindo o banco de dados deve ser SQL Server versão 7.0 ou posterior.

  > [!NOTE]
  > [!OBSERVAçãO] Servidores vinculados não são transferidos durante a operação de transferência de banco de dados.

Para executar a ação **TransferirBancoDeDadosSQL** em um módulo do VBA (Visual Basic for Applications), use o método **TransferSQLDatabase** do objeto **DoCmd**.

