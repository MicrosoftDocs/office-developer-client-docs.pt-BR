---
title: Ação da macro CopiarArquivoDeBancodeDados
TOCTitle: CopyDatabaseFile macro action
ms:assetid: e6320b55-946b-9efc-9b64-b86513801a37
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835963(v=office.15)
ms:contentKeyID: 48548373
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 330ae78b86c678b675cfd44afa75f72348ac582f
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998907"
---
# <a name="copydatabasefile-macro-action"></a>Ação da macro CopiarArquivoDeBancodeDados

**Aplica-se a**: Access 2013, o Office 2013

Você pode usar a ação **CopiarArquivoDeBancodeDados** para fazer uma cópia do banco de dados atual do Microsoft SQL Server 7.0 ou versões posteriores conectado ao projeto do Access. Access desanexa o banco de dados atual e, em seguida, anexa-o ao servidor de destino. Para obter mais informações sobre como desanexar e anexar um banco de dados, consulte a documentação do SQL Server.

> [!NOTE]
> [!OBSERVAçãO] This action will not be allowed if the database is not trusted. 


## <a name="setting"></a>Configuração

A ação **CopiarArquivoDeBancodeDados** tem os seguintes argumentos.

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
<td><p><strong>Nome de Arquivo do Banco de Dados</strong></p></td>
<td><p>O nome do novo Arquivo de Dados Mestre. O caminho padrão do arquivo é o local atual do arquivo de projeto do Access (.adp).</p></td>
</tr>
<tr class="even">
<td><p><strong>Substituir Arquivo Existente</strong></p></td>
<td><p>Especifica se será ou não substituído um arquivo existente pelo mesmo nome. Se estiver definido como <strong>Sim</strong> e o nome de arquivo já existir , o arquivo será substituído. Se estiver definido como <strong>Não</strong> e o nome de arquivo já existir, o arquivo não será substituído e a ação falhará. Se o arquivo ainda não existir, essa configuração será ignorada. O padrão é <strong>Sim</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Desconectar Todos os Usuários</strong></p></td>
<td><p>Especifica se o Access deve ou não remover os usuários do banco de dados. Se estiver definido como <strong>Sim</strong>, quaisquer usuários conectados ao banco de dados atual serão desconectados para que a operação de banco de dados de cópia possa prosseguir. Se estiver definido como <strong>Não</strong> e um ou mais usuários estiverem conectados ao banco de dados, a operação de banco de dados de cópia falhará. O padrão é <strong>Não</strong>. 

</p><p><strong>Aviso</strong>: desconectar usuários de um banco de dados, sem aviso adequado pode levar à perda de dados.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

A operação de cópia é síncrona, por isso não será possível executar outras operações enquanto a cópia do banco de dados não for concluída.

A ação **CopiarArquivoDeBancodeDados** não só copia os dados, as definições de dados e os objetos de banco de dados, como também copia propriedades estendidas, como valores padrão, restrições de texto e valores de pesquisa.

Requisitos para copiar um banco de dados:

- Todos os aplicativos e usuários precisam ser desconectados antes de copiar o arquivo de banco de dados.

- Todos os objetos e modos de exibição, com exceção do Painel de Navegação, precisam ser fechados.

- O banco de dados atual não pode ser replicado.

- O banco de dados de servidor de origem precisa ser o Microsoft SQL Server 7.0 ou versão posterior, ou o SQL Server 2000 Desktop Engine executado em um computador local.

- O banco de dados do SQL Server no servidor de origem precisa consistir em um único arquivo.

- Você precisa ser membro da função sysadmin nos computadores SQL Server de origem e de destino.

Para executar a ação **CopiarArquivoDeBancodeDados** em um módulo do Visual Basic for Applications, use o método **CopyDatabaseFile** do objeto **DoCmd**.

