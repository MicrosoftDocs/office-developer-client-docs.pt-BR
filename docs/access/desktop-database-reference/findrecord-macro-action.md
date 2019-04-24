---
title: Ação da macro EncontrarRegistro
TOCTitle: FindRecord macro action
ms:assetid: 379e3dda-cb7d-a294-29b1-c6ce9a62ba8a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192494(v=office.15)
ms:contentKeyID: 48544199
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm7496
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 086993095daef3ff4ad87aed9f572a09124a9d31
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292368"
---
# <a name="findrecord-macro-action"></a>Ação da macro EncontrarRegistro

**Aplica-se ao:** Access 2013, Office 2013

Você pode usar a ação **EncontrarRegistro** para localizar a primeira instância de dados que atende aos critérios especificados pelos argumentos **EncontrarRegistro**. Esses dados podem estar no registro atual, em um registro sucessivo ou anterior, ou no primeiro registro. Você pode localizar registros na folha de dados da tabela ativa, na folha de dados de consulta ou no formulário.

## <a name="setting"></a>Configuração

A ação **EncontrarRegistro** tem os seguintes argumentos.

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
<td><p><strong>Localizar</strong></p></td>
<td><p>Especifica os dados que serão localizados no registro. Insira o texto, o número ou a data que você deseja localizar ou digite uma expressão, que é precedida por um sinal de<strong>=</strong>igual (), na seção <strong>Localizar</strong> , na seção <strong>argumentos da ação</strong> do painel Construtor de macros. Você pode usar caracteres curinga. Esse é um argumento obrigatório.</p></td>
</tr>
<tr class="even">
<td><p><strong>Match</strong></p></td>
<td><p>Especifica onde os dados estão localizados no campo. Você pode especificar uma pesquisa dos: dados em qualquer parte do campo (<strong>Qualquer Parte do Campo</strong>); dados que preenchem o campo inteiro (<strong>Campo Inteiro</strong>); ou dados localizados no início do campo (<strong>Início do Campo</strong>). O padrão é <strong>Campo Inteiro</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Diferenciar Maiúsc. de Minúsc.</strong></p></td>
<td><p>Especifica se a pesquisa diferencia maiúsculas de minúsculas. Clique em <strong>Sim</strong> (conduzir uma pesquisa com diferenciação de maiúsculas e minúsculas) ou <strong>Não</strong> (pesquisar sem fazer coincidir exatamente as letras maiúsculas e minúsculas). O padrão é <strong>Não</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>Search</strong></p></td>
<td><p>Especifica se a pesquisa continua partindo do registro atual e sobe até o início dos registros (<strong>Acima</strong>); desce até o final dos registros (<strong>Abaixo</strong>); ou desce até o final dos registros e partindo do início dos registros até o registro atual, para que todos os registros sejam pesquisados (<strong>Todos</strong>). O padrão é <strong>Tudo</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Pesquisar como Formatado</strong></p></td>
<td><p>Especifica se a pesquisa inclui dados formatados. Clique em <strong>Sim</strong> (o Microsoft Office Access 2007 pesquisa os dados à medida que são formatados e exibidos no campo) ou <strong>Não</strong> (o Access pesquisa os dados à medida que são armazenados no banco de dados, o que nem sempre é o mesmo que quando são exibidos). O padrão é <strong>Não</strong>. Você pode usar esse recurso para restringir a pesquisa a dados de um formato específico. Por exemplo, clique em <strong>Sim</strong> e digite <strong>1.234</strong> no argumento <strong>Localizar</strong> para localizar um valor de 1.234 em um campo formatado para incluir pontos. Clique em <strong>Não</strong> se desejar digitar <strong>1234</strong> para pesquisar dados nesse campo. Para pesquisar datas, clique em <strong>Sim</strong> para localizar uma data exatamente como ela está formatada, como 08-Julho-2003. Se você clicar em <strong>Não</strong>, digite a data do argumento <strong>Localizar</strong> no formato definido nas configurações regionais do Painel de Controle do Windows. Esse formato é mostrado na caixa <strong>Formato de data abreviada</strong> localizada na guia <strong>Data</strong> das configurações regionais. Por exemplo, se a caixa <strong>Formato de data abreviada</strong> estiver definida como <strong>M/d/aa</strong>, você poderá digitar 7/8/03, e o Access localizará todas as entradas em um campo Data que correspondem a 8 de julho de 2003, independentemente de como esse campo esteja formatado.</p>
<p><strong>Observação</strong>: o argumento <strong>Pesquisar como formatado</strong> tem efeito somente se o campo atual for um controle acoplado, o argumento <strong>Match</strong> estiver definido como <strong>campo inteiro</strong>, o argumento <strong>somente campo atual</strong> será definido como <strong>Sim</strong>e a <strong>correspondência </strong>O argumento Case é definido como <strong>não</strong>.</p>
<p>Se você definiu <strong>Diferenciar Maiúsc. de Minúsc.</strong> como <strong>Sim</strong>, ou <strong>Somente Campo Atual</strong> como <strong>Não</strong>, também precisará definir <strong>Pesquisar como Formatado</strong> como <strong>Sim</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>Somente Campo Atual</strong></p></td>
<td><p>Especifica se a pesquisa está confinada no campo atual em cada registro ou se inclui todos os campos de cada registro. A pesquisa no campo atual é mais rápida. Clique em <strong>Sim</strong> (confinar a pesquisa no campo atual) ou <strong>Não</strong> (pesquisar em todos os campos de cada registro). O padrão é <strong>Sim</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Localizar Primeiro</strong></p></td>
<td><p>Especifica se a pesquisa começa no primeiro registro ou no atual. Clique em <strong>Sim</strong> (começar no primeiro registro) ou <strong>Não</strong> (começar no registro atual). O padrão é <strong>Sim</strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

Quando uma macro é executada na ação **EncontrarRegistro**, o Access pesquisa os dados especificados nos registros (a ordem da pesquisa é determinada pela configuração do argumento **Pesquisar** ). Quando o Access localiza os dados especificados, eles são selecionados no registro.

A ação **EncontrarRegistro** equivale a clicar em **Localizar** na guia **Página Inicial**, e seus argumentos são os mesmos das opções na caixa de diálogo **Localizar e Substituir**. Se você definir os argumentos **EncontrarRegistro** no painel Construtor de Macros e executar a macro, verá as opções correspondentes selecionadas na caixa de diálogo **Localizar e Substituir** ao clicar em **Localizar**.

O Access retém os argumentos **EncontrarRegistro** mais recentes durante uma sessão de banco de dados para que não seja necessário inserir os mesmos critérios várias vezes à medida que são executadas operações subsequentes com a ação **EncontrarRegistro**. Se você deixar um argumento em branco, o Access usará a configuração mais recente do argumento, conforme definida por uma ação **EncontrarRegistro** anterior ou na caixa de diálogo **Localizar e Substituir**.

Quando você deseja localizar um registro usando uma macro, use a ação **EncontrarRegistro**, e não a ação **ExecutarComandodeMenu** com o respectivo argumento definido para executar o comando **Localizar**.

> [!NOTE]
> [!OBSERVAçãO] Embora a ação **EncontrarRegistro** corresponda ao comando **Localizar** na guia **Página Inicial** para tabelas, consultas e formulários, ela não corresponde ao comando **Localizar** no menu **Editar** da janela Código. Não é possível usar a ação **EncontrarRegistro** para pesquisar texto em módulos.

Se o texto selecionado no momento for o mesmo do texto de pesquisa quando a ação **EncontrarRegistro** for executada, a pesquisa começará imediatamente após a seleção, no mesmo campo da seleção e no mesmo registro. Caso contrário, começará no início do registro atual. Isso permite localizar várias instâncias dos mesmos critérios de pesquisa que podem aparecer em um único registro.

Entretanto, observe que, se você usar um botão de comando para executar uma macro que contém a ação **EncontrarRegistro**, a primeira instância dos critérios de pesquisa será localizada várias vezes. Esse comportamento ocorre porque clicar no botão de comando remove o foco do campo que contém o valor correspondente. A ação **EncontrarRegistro** começará a pesquisar partindo do início do registro. Para evitar esse problema, execute a macro usando uma técnica que não altera o foco, como um botão de barra de ferramentas personalizado ou uma combinação de teclas definida em uma macro AutoKeys. Ou então, defina o foco na macro para o campo que contém os critérios de pesquisa antes de executar a ação **EncontrarRegistro**.

<table>
<thead>
<tr class="header">
<th><img src="media/access-alert-security.gif" title="Observação de segurança" alt="Security note" /><strong>Observação de Segurança</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Avoid using the <strong>SendKeys</strong> statement or an AutoKeys macro with sensitive or confidential information. A malicious user could intercept the keystrokes and compromise the security of your computer and data.</td>
</tr>
</tbody>
</table>

O mesmo comportamento também ocorre se você usa um botão de comando para executar uma macro que contém a ação **EncontrarPróximo**.

Para executar a ação **EncontrarRegistro** em um módulo do VBA (Visual Basic for Applications), use o método **FindRecord** do objeto **DoCmd**.

Para pesquisas mais complexas, convém usar a ação de macro **ProcurarRegistro**.

