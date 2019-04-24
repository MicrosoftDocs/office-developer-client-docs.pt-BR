---
title: Propriedade Connection. Connect (DAO)
TOCTitle: Connect Property
ms:assetid: 58b514a2-91cd-7918-cba5-15d71c2457a6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194335(v=office.15)
ms:contentKeyID: 48545001
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e44ce5b4acf58f3f9d9e887d0136baed64c8e227
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295923"
---
# <a name="connectionconnect-property-dao"></a>Propriedade Connection. Connect (DAO)


**Aplica-se ao:** Access 2013, Office 2013

Define ou retorna um valor que fornece informações sobre a origem de uma conexão aberta. **String** de leitura/gravação.

## <a name="syntax"></a>Sintaxe

*expressão* . Ao

*expressão* Uma variável que representa um objeto **Connection** .

## <a name="remarks"></a>Comentários

A definição da propriedade **Connect** é uma **String** composta de um especificador do tipo de banco de dados e zero ou mais parâmetros separados por ponto-e-vírgulas. A propriedade **Connect** passa informações adicionais para ODBC e determinados drivers ISAM conforme necessário.

Para executar uma consulta passagem SQL em uma tabela vinculada ao arquivo de banco de dados do Microsoft Access, você deve primeiro definir a propriedade **Connect** do banco de dados da tabela vinculada para uma sequência de conexão ODBC válida.

Para um objeto **TableDef** que representa uma tabela vinculada, a configuração da propriedade **Connect** consiste em uma ou duas partes (um especificador de tipo de banco de dados e um caminho para o banco de dados), que terminam com um ponto-e-vírgula.

O caminho, como mostrado na tabela a seguir, é um caminho completo para o diretório que contém os arquivos de banco de dados e deve ser precedido pelo identificador DATABASE=. Em alguns casos (como nos bancos de dados do mecanismo de banco de dados do Microsoft Excel e do Microsoft Access), você deverá incluir um nome de arquivo específico no argumento do caminho do banco de dados.

A tabela a seguir mostra os tipos possíveis de bancos de dados e seus especificadores e caminhos correspondentes para a configuração da propriedade **Connect**.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Tipo de banco de dados</p></th>
<th><p>Especificado</p></th>
<th><p>Exemplo</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Banco de dados do Microsoft Access</p></td>
<td><p>[banco de dados];</p></td>
<td><p>unidade: \ path\filename</p></td>
</tr>
<tr class="even">
<td><p>dBASE III</p></td>
<td><p>dBASE III;</p></td>
<td><p>unidade: \ caminho</p></td>
</tr>
<tr class="odd">
<td><p>dBASE IV</p></td>
<td><p>dBASE IV;</p></td>
<td><p>unidade: \ caminho</p></td>
</tr>
<tr class="even">
<td><p>dBASE 5</p></td>
<td><p>dBASE 5.0;</p></td>
<td><p>unidade: \ caminho</p></td>
</tr>
<tr class="odd">
<td><p>Paradox 3.x</p></td>
<td><p>Paradox 3.x;</p></td>
<td><p>unidade: \ caminho</p></td>
</tr>
<tr class="even">
<td><p>Paradox 4.x</p></td>
<td><p>Paradox 4.x;</p></td>
<td><p>unidade: \ caminho</p></td>
</tr>
<tr class="odd">
<td><p>Paradox 5.x</p></td>
<td><p>Paradox 5.x;</p></td>
<td><p>unidade: \ caminho</p></td>
</tr>
<tr class="even">
<td><p>Microsoft Excel 3.0</p></td>
<td><p>Excel 3.0;</p></td>
<td><p>unidade: \ path\filename.xls</p></td>
</tr>
<tr class="odd">
<td><p>Microsoft Excel 4.0</p></td>
<td><p>Excel 4.0;</p></td>
<td><p>unidade: \ path\filename.xls</p></td>
</tr>
<tr class="even">
<td><p>Microsoft Excel 5.0 ou Microsoft Excel 95</p></td>
<td><p>Excel 5.0;</p></td>
<td><p>unidade: \ path\filename.xls</p></td>
</tr>
<tr class="odd">
<td><p>Microsoft Excel 97</p></td>
<td><p>Excel 8.0;</p></td>
<td><p>unidade: \ path\filename.xls</p></td>
</tr>
<tr class="even">
<td><p>Lotus 1-2-3 WKS e WK1</p></td>
<td><p>Lotus WK1;</p></td>
<td><p>unidade: \ path\filename.WK1</p></td>
</tr>
<tr class="odd">
<td><p>Lotus 1-2-3 WK3</p></td>
<td><p>Lotus WK3;</p></td>
<td><p>unidade: \ path\filename.WK3</p></td>
</tr>
<tr class="even">
<td><p>Lotus 1-2-3 WK4</p></td>
<td><p>Lotus WK4;</p></td>
<td><p>unidade: \ path\filename.WK4</p></td>
</tr>
<tr class="odd">
<td><p>HTML Import</p></td>
<td><p>HTML Import;</p></td>
<td><p>unidade: \ path\filename</p></td>
</tr>
<tr class="even">
<td><p>HTML Export</p></td>
<td><p>HTML Export;</p></td>
<td><p>unidade: \ caminho</p></td>
</tr>
<tr class="odd">
<td><p>Texto</p></td>
<td><p>Textos</p></td>
<td><p>unidade: \ caminho</p></td>
</tr>
<tr class="even">
<td><p>Connectivity</p></td>
<td><p>Connectivity DATABASE = database; UID = User; PWD = senha; DSN = DataSourceName; [LOGINTIMEOUT = segundos;]</p></td>
<td><p>Nenhum</p></td>
</tr>
<tr class="odd">
<td><p>Microsoft Exchange</p></td>
<td><p>Exchange 4,0; MAPILEVEL = FolderPath; [TABLETYPE = {0 | 1}]; [PROFILE = Profile;] [PWD = senha;] [DATABASE = database;]</p></td>
<td><p>unidade: \ path\filename</p></td>
</tr>
</tbody>
</table>


Se o especificador for apenas "ODBC;", o driver ODBC exibirá uma caixa de diálogo listando todos os nomes registrados de fonte de dados ODBC para que o usuário possa selecionar um banco de dados.

Se for necessária uma senha que não foi fornecida na definição da propriedade **Connect**, será exibida uma caixa de diálogo de logon na primeira vez que uma tabela for acessada pelo driver ODBC e mais uma vez se a conexão for fechada e aberta novamente.

Para os dados no Microsoft Exchange, a chave MAPILEVEL necessária deve ser definida como o caminho da pasta totalmente resolvido (por exemplo, "Mailbox - Pat SmithIAlpha/Today"). O caminho não inclui o nome da pasta que será aberta como uma tabela; em vez disso, o nome da pasta deve ser especificado como o argumento **** Name para o método CreateTable. A chave TABLETYPE deverá ser definida como "0" para abrir uma pasta (padrão) ou "1" para abrir um catálogo de endereços. A chave PROFILE é o padrão para o perfil usado no momento.

Para as tabelas base em um banco de dados do Microsoft Access, a definição da propriedade **Connect** será uma sequência de caracteres com comprimento zero ("").

Você pode definir a propriedade **Connect** para um objeto **Database** fornecendo um argumento Source para o método **OpenDatabase** . Você pode verificar a configuração para determinar o tipo, o caminho, a identificação do usuário, a senha ou a fonte de dados ODBC do banco de dados.

Em um objeto **QueryDef** no espaço de trabalho do Microsoft Access, você pode usar a propriedade **Connect** com a propriedade ReturnsRecords para criar uma consulta passagem ODBC SQL. O databasetype da cadeia de conexão é "ODBC;", e o lembrete da sequência contém informações específicas para o driver ODBC utilizado para acessar os dados remotos. Para obter mais informações, consulte a documentação do driver específico.


> [!NOTE]
> - Defina a propriedade **Connect** antes de definir a propriedade **ReturnsRecords**.
> - É necessário ter permissões de acesso para o computador que contém o servidor do banco de dados que você está tentando acessar.


