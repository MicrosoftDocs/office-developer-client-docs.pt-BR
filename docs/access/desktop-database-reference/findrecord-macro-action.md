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
ms.openlocfilehash: 19b6c80af2bcee9ca3dbe51bbbcf56343f33d550
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25937607"
---
# <a name="findrecord-macro-action"></a>Ação da macro EncontrarRegistro

**Aplica-se a**: Access 2013, o Office 2013

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
<td><p>Especifica os dados que você deseja localizar no registro. Insira o texto, número ou data que você deseja localizar ou digite uma expressão, que é precedida por um sinal de igualdade (<strong>=</strong>), na caixa <strong>Localizar</strong> na seção <strong>Argumentos da ação</strong> do painel de tarefas do construtor de macros. Você pode usar caracteres curinga. Este é um argumento obrigatório.</p></td>
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
<td><p><strong>Pesquisar</strong></p></td>
<td><p>Especifica se a pesquisa continua partindo do registro atual e sobe até o início dos registros (<strong>Acima</strong>); desce até o final dos registros (<strong>Abaixo</strong>); ou desce até o final dos registros e partindo do início dos registros até o registro atual, para que todos os registros sejam pesquisados (<strong>Todos</strong>). O padrão é <strong>Tudo</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Pesquisar como Formatado</strong></p></td>
<td><p>Especifica se a pesquisa inclui dados formatados. Clique em <strong>Sim</strong> (Microsoft Office Access 2007 procurará os dados como é exibido no campo e formatado) ou <strong>não</strong> (Access procura os dados como ele está armazenado no banco de dados, não é sempre o mesmo como ele é exibido). O padrão é <strong>Não</strong>. Você pode usar esse recurso para restringir a pesquisa aos dados em um determinado formato. Por exemplo, clique em <strong>Sim</strong> e digite <strong>1.234</strong> no argumento <strong>Localizar</strong> para localizar um valor 1.234 em um campo formatado para incluir vírgulas. Clique em <strong>não</strong> se você quiser digitar <strong>1234</strong> para pesquisar os dados nesse campo. Para pesquisar datas, clique em <strong>Sim</strong> para localizar uma data exatamente como ela está formatada, como 08 de julho de 2003. Se você clicar em <strong>não</strong>, digite a data para o argumento <strong>Localizar</strong> no formato definido nas configurações regionais no painel de controle do Windows. Esse formato é mostrado na caixa <strong>formato de data curta</strong> encontrada na guia <strong>Data</strong> nas configurações regionais. Por exemplo, se a caixa de <strong>formato de data curta</strong> estiver definida como <strong>m/aa</strong>, você pode inserir 7/8/03 e Access irá localizar todas as entradas em um campo de data que correspondem à 8 de julho de 2003, independentemente de como esse campo é formatado.</p>

> [!NOTE]
> O argumento **Pesquisar como Formatado** funcionará somente se o campo atual for um controle associado, o argumento **Coincidir** estiver definido como **Campo Inteiro**, o argumento **Somente Campo Atual** estiver definido como **Sim** e o argumento **Diferenciar Maiúsc. de Minúsc.** estiver definido como **Não**.


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
<th><img src="media/access-alert-security.gif" title="Observação sobre segurança" alt="Security note" /><strong>Observação de segurança</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>
      Avoid using the <strong>SendKeys</strong> statement or an AutoKeys macro with sensitive or confidential information. A malicious user could intercept the keystrokes and compromise the security of your computer and data.
</td>
</tr>
</tbody>
</table>

O mesmo comportamento também ocorre se você usa um botão de comando para executar uma macro que contém a ação **EncontrarPróximo**.

Para executar a ação **EncontrarRegistro** em um módulo do VBA (Visual Basic for Applications), use o método **FindRecord** do objeto **DoCmd**.

Para pesquisas mais complexas, convém usar a ação de macro **ProcurarRegistro**.

