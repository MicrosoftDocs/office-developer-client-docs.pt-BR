---
title: Níveis de segurança, implantação de email e modelos de formulário remotos
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7fc438ad-ae26-3632-3444-371537eaecb3
description: O Microsoft InfoPath oferece suporte à migração de modelos de formulário de um local para outro, enviando-os como um anexo a uma mensagem de email e criando modelos de formulário de Confiança Total que são assinados ou instalados digitalmente.
ms.openlocfilehash: 799f2b19bfc4daa4a177d789a811d20ca09e7153
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396873"
---
# <a name="security-levels-email-deployment-and-remote-form-templates"></a>Níveis de segurança, implantação de email e modelos de formulário remotos

O Microsoft InfoPath oferece suporte à migração de modelos de formulário de um local para outro, enviando-os como um anexo a uma mensagem de email e criando modelos de formulário de Confiança Total que são assinados ou instalados digitalmente.
  
## <a name="security-levels"></a>Níveis de segurança

Os modelos de formulário podem ter um destes três níveis de segurança, dependendo de onde o formulário está localizado. Esses três níveis de segurança são descritos em detalhes nas seções a seguir. 
  
### <a name="restricted"></a>Restrito

O modo de segurança restrito não permite a comunicação fora do modelo de formulário. Este nível de segurança destina-se a evitar que formulários prejudiciais transmitam dados do seu computador para um invasor mal-intencionado. Ao executar neste modo de segurança, os seguintes recursos não funcionarão:
  
- Painéis de tarefas HTML  
- Consulta do SharePoint
- Envio do SharePoint
- Consulta de arquivo XML
- Consulta de banco de dados
- Envio de banco de dados
- Consulta de serviço Web
- Envio de serviço Web
- Envio de código personalizado
- Envio de ambiente de hospedagem
- Controles ActiveX
- Funções
- Fluxo de trabalho do SharePoint
- Regras que abrem um Novo documento
- Código gerenciado
- Modo de exibição de impressão externa
- Imagens vinculadas
    
### <a name="domain"></a>Domínio

O nível de segurança do domínio restringe um formulário a um determinado domínio da Internet, e suas permissões são restritas às configurações do Internet Explorer da zona onde o domínio está localizado. O formulário pode se comunicar com outras fontes de dados dentro de seu próprio domínio, mas, geralmente, não tem permissão para recuperar dados de outros domínios a menos que a zona permita a comunicação entre domínios. Esse é o nível mínimo de segurança para modelos de formulário compatíveis com o navegador.
  
### <a name="full-trust"></a>Confiança Total

O nível de segurança de Confiança total permite executar um formulário com confiança total no computador no qual o formulário será usado. Esse nível de segurança só pode ser usado se você estiver trabalhando com um formulário localizado em um servidor assinado com uma assinatura que corresponda a um editor raiz confiável em seu computador ou se estiver instalando o formulário. Os dois métodos exigem a configuração do atributo **requireFullTrust** como "yes". Usando essa configuração, o formulário pode acessar chamadas do modelo de objeto, como salvar arquivo. Além disso, determinados prompts de segurança que são exibidos ao executar em um nível de segurança mais restritivo são desativados. 
  
> [!NOTE]
> Todos os formulários gerados no designer do InfoPath têm um nível de segurança associado a eles. O InfoPath abre formulários em seu nível de segurança associado. Se o nível de segurança associado ao formulário for maior que o nível de segurança que pode ser concedido a ele, o formulário não será aberto. 
  
O nível de segurança de Confiança total só pode ser definido para modelos de formulário instalados ou assinados. Caso contrário, o nível máximo de confiança será Domínio. O InfoPath não definirá um nível de segurança como Confiança total automaticamente.
  
Os formulários recebem níveis de segurança tendo como base o local onde o formulário é aberto.
  
## <a name="trust-levels"></a>Níveis de confiança

O nível mais alto de confiança que pode ser concedido a um modelo de formulário é determinado pelo código Aberto no local e por outro código de verificação, conforme descrito na tabela a seguir. Os atributos listados na tabela (por exemplo, HTTP, UNC, *requireFullTrust*) são entradas usadas para determinar o nível de confiança que pode ser concedido a um formulário e se aplicam a formulários abertos no cliente do InfoPath. 
  
|Nível mais alto de confiança concedido|Confiança Total|Computador cliente (área restrita)|Intranet (área restrita)|Internet (área restrita)|Restrito|
|:-----|:-----:|:-----:|:-----:|:-----:|:-----:|
|**arquivo: Caminho de Acesso=Aberto no local** <br/> |||X  <br/> |||
|**arquivo: Caminho de Acesso\<\>Aberto no local ou sem Caminho de acesso (independentemente da procedência do formulário)** <br/> |||||X  <br/> |
|**Aberto no local: Intranet HTTP ou HTTPS** <br/> |||X  <br/> |||
|**Aberto no local: Internet HTTP ou HTTPS** <br/> ||||X  <br/> ||
|**Aberto no local: UNC** <br/> |||X  <br/> |||
|**Modelo instalado (requireFullTrust="yes")** <br/> |X  <br/> |||||
|**Installed Template (requireFullTrust="no")** <br/> ||X  <br/> ||||
|**Modelo com o certificado do fornecedor confiável** <br/> |X  <br/> |||||
|**Arquivos de formulário exportados** <br/> |||X  <br/> |||
   
## <a name="form-open-behavior"></a>Comportamento de abertura do formulário

Todos os arquivos de formulário abertos no editor do InfoPath são limitados por um conjunto de condições que determinam o nível de segurança no qual o formulário será aberto e se ele será aberto. Quando um formulário do InfoPath é aberto no editor, ele será aberto com um nível de segurança apropriado ou não será carregado. Se um formulário solicitar um nível de segurança mais alto do que aquele que pode ser concedido (um formulário pode solicitar um nível de segurança específico usando o atributo **trustLevel** ou **requireFullTrust**), ele não poderá ser carregado. Caso contrário, ele será carregado com o nível de segurança solicitado. Se o modelo de formulário não puder abrir com o nível de segurança solicitado, o usuário não conseguirá abrir o formulário e receberá uma mensagem de erro. 
  
A tabela a seguir descreve as condições necessárias para abrir um formulário em cada nível de segurança e o comportamento resultante quando o usuário tenta abrir o formulário.
  
|Editor abre/falha|Confiança Total (requireFullTrust="yes")|Confiança de Domínio (trustLevel="Domain" ou em branco)|Restrito (trustLevel="Restricted")|
|:-----|:-----|:-----|:-----|
|**Confiável (certificado instalado ou confiável)** <br/> |O editor é aberto no nível de Confiança Total  <br/> |N/D  <br/> |N/D  <br/> |
|**Confiança de domínio: Computador cliente** <br/> |Falha ao abrir  <br/> |O editor é aberto no nível de Domínio  <br/> |O editor é aberto no nível Restrito  <br/> |
|**Confiança de domínio: Intranet** <br/> |Falha ao abrir  <br/> |O editor é aberto no nível de Domínio  <br/> |O editor é aberto no nível Restrito  <br/> |
|**Confiança de domínio: Internet** <br/> |Falha ao abrir  <br/> |O editor é aberto no nível de Domínio  <br/> |O editor é aberto no nível Restrito  <br/> |
|**Restrito** <br/> |Falha ao abrir  <br/> |Falha ao abrir  <br/> |O editor é aberto no nível Restrito  <br/> |
   
## <a name="specifying-a-security-level"></a>Como especificar um nível de segurança

O designer de formulários do InfoPath seleciona automaticamente o nível de segurança apropriado (Restrito ou Domínio) com base nos recursos que você está usando no formulário. A configuração da segurança é sempre a mais restritiva possível, começando em Restrito, para ajudar a garantir um nível maior de proteção para você e seus dados. Os usuários podem substituir manualmente essa configuração automatizada para escolher um nível de segurança mais apropriado para o formulário seguindo estas etapas:
  
1. Clique na guia **Arquivo** e em **Opções de Formulário**. Depois, clique na guia **Informações**. 
    
2. Na lista **Categorias**, clique em **Segurança e Confiança**.
    
3. Desmarque a caixa de seleção **Determinar automaticamente o nível de segurança (recomendado)**. 
    
4. Escolha o nível de segurança desejado.
    
## <a name="mail-deployment-and-browser-enabled-form-templates"></a>Implantação do email e modelos de formulário habilitados para navegador

O InfoPath permite enviar seus modelos de formulário como anexos a uma mensagem de email e movê-los de um local para outro. A implantação do email é uma maneira fácil e eficaz de distribuir formulários para uso entre escritórios e também para implantar formulários para usuários remotos.
  
Como alternativa, se você tiver o Microsoft SharePoint Server 2010 com o InfoPath Forms Services disponível, poderá criar modelos de formulário que permitam aos usuários que não têm o InfoPath instalado preencher formulários em um navegador da Web.
  
## <a name="understanding-form-identity"></a>Noções básicas sobre a identidade do formulário

No designer do InfoPath, todos os formulários são criados com uma identidade. Essas informações de identidade ajudam o InfoPath a associar formulários a modelos de formulário no cache e a recuperar atualizações de formulários quando elas são postadas em um local compartilhado. Por padrão, o InfoPath cria duas identidades para modelos de formulário: uma ID de formulário e um Caminho de acesso. 
  
### <a name="form-id"></a>ID de formulário

A ID de formulário é um identificador exclusivo baseado em um prefixo, o nome do formulário e o namespace do formulário. O identificador deve ser um nome exclusivo que possa ser usado para associar corretamente os arquivos de formulário ao modelo de formulário associado no cache do computador cliente. A ID de formulário for especificada como o atributo de nome (por exemplo, `name="urn:MyForm:MyCompany:Template1:myXSD-1583-78-G3V94-23-47"`) no arquivo de definição de formulário (.xsf). 
  
### <a name="access-path"></a>Caminho de Acesso

O Caminho de Acesso é um identificador de local usado para determinar o local correto do modelo de formulário e também o local para receber atualizações. Quando salvo ou publicado, o local onde o modelo de formulário é salvo ou publicado se torna o Caminho de Acesso padrão. Sempre que um formulário é aberto no computador cliente, o formulário tenta se associar a um formulário em cache. Ele tentará fazer isso na seguinte ordem:
  
1. Procurar um modelo de formulário totalmente confiável com uma ID de formulário correspondente.
    
2. Procurar um modelo de formulário em cache com um Caminho de acesso correspondente.
    
3. Procurar por um modelo de formulário em cache com uma ID de formulário correspondente.
    
Uma vez correspondido, o formulário será aberto com o modelo de formulário associado. Nos casos em que a correspondência foi feita com um Caminho de Acesso, o InfoPath usará o Caminho de acesso para recuperar atualizações para o modelo de formulário. Esse método simplifica a administração, manutenção e atualização de formulários pelas empresas. Nos casos em que a correspondência não pode ser feita e o nível de confiança for Domínio, o formulário não será aberto. O Caminho de Acesso é especificado como o atributo **publishUrl** no arquivo de definição de formulário (.xsf). 
  
Assim como há duas propriedades de identificação para cada modelo de formulário, há um conjunto de heurísticas para determinar especificamente as entradas resultantes no cache, com base na condição do modelo de formulário (se ele tem um Caminho de Acesso, uma ID de formulário ou ambos) e o estado da conexão de rede.
  
## <a name="designing-a-form-to-send-as-an-attachment-to-an-email-message"></a>Criar um formulário para enviar como um anexo a uma mensagem de email

Todos os formulários criados no designer do InfoPath podem ser enviados aos usuários como um anexo em uma mensagem de email. A implantação do email é uma maneira fácil e eficaz de distribuir formulários para uso entre escritórios e também para implantar formulários para usuários remotos.
  
### <a name="to-mail-a-form-template-to-other-users"></a>Para enviar um modelo de formulário para outros usuários via email

1. Clique na guia **Arquivo**, clique em **Publicar** e clique no botão **Email**. 
    
2. Preencha as próximas duas páginas do **Assistente de Publicação** clicando em **Avançar** para continuar após cada página e clique em **Publicar**.
    
3. Uma mensagem de email é exibida permitindo que você preencha a lista de destinatários e quaisquer instruções adicionais que você possa ter para eles.
    
4. Ao concluir, clique em **Enviar**. O modelo de formulário e o formulário serão anexados à mensagem.
    
## <a name="email-deployment-restricted-domain-and-full-trust-form-templates"></a>Implantação do email: modelos de formulário Restrito, de Domínio e de Confiança Total

A implantação do email de modelos de formulário Restritos permite que formulários dinâmicos sem conexões de dados sejam abertos em qualquer lugar. Os destinatários podem abrir modelos de formulário enviados como anexos de email diretamente do Microsoft Outlook 2010 ou de qualquer local onde o destinatário tenha salvo o anexo. Além disso, o Outlook 2010 permite que os usuários editem formulários diretamente na mensagem.
  
Os modelos de formulário com o nível de confiança de Domínio devem ser abertos a partir do local publicado, mas, ao publicar em uma lista de destinatários de email no Assistente de Publicação, eles podem ser enviados como um anexo em uma mensagem de email. Quando o anexo é aberto, ele funciona como um link para o local real publicado do modelo. O modelo de formulário nesse local é o que é realmente aberto no editor do InfoPath.
  
Usar um modelo de formulário no nível do Domínio enviado como um anexo de email é semelhante a usar qualquer outro tipo de documento, como uma pasta de trabalho do Microsoft Excel ou um documento do Microsoft Word. Basta o usuário clicar no formulário para abri-lo e usá-lo. Além disso, todos os benefícios das atualizações no nível do Domínio estão disponíveis para os usuários.
  
É possível enviar modelos de formulário por email que solicitam acesso de Confiança Total. No entanto, esses modelos devem ser assinados ou não poderão ser abertos. Os modelos de formulário que solicitam acesso Restrito ou de Domínio não precisam ser assinados para serem enviados como um anexo de email. O InfoPath não analisa ou verifica a assinatura, mesmo se o modelo estiver assinado, exceto para ver se ela pode ser atualizada automaticamente. Você pode assinar digitalmente um modelo de formulário de Domínio ou Restrito e ainda manter o recurso de atualização automática. Neste caso, a assinatura digital impedirá que qualquer mensagem de conflito de cache seja exibida.
  
## <a name="sharing-forms-by-email-message-or-from-a-common-shared-location"></a>Compartilhar formulários por mensagem de email ou de um local compartilhado comum

Certas questões devem ser consideradas quando você está criando um formulário que será implantado através de uma mensagem de email.
  
- **O formulário será atualizado regularmente?** Se você estiver desenvolvendo um formulário que deverá ser atualizado regularmente, o formulário deverá ser publicado em um local compartilhado antes de ser enviado a outros usuários. Essa prática permite que você atualize o formulário publicando versões mais recentes no local compartilhado, mas também permite distribuir imediatamente o modelo de formulário para usuários que não tenham acesso ao local compartilhado. 
    
   Se um formulário for atualizado e distribuído por mensagem de email, os usuários receberão uma mensagem de conflito de cache quando tentarem abrir o novo formulário, se tiverem uma versão mais antiga armazenada no computador e o Caminho de acesso tiver sido alterado. O usuário será solicitado a escolher a versão que deseja usar. Mesmo que o formulário atualizado seja o mesmo do computador do usuário, o usuário receberá uma mensagem de conflito de cache e será solicitado a escolher a cópia que deseja usar. A prática recomendada a ser usada na última opção é compartilhar o formulário a partir de um local compartilhado.
    
- **Seu formulário acessa uma conexão de dados ou usa outros recursos não suportados no nível de segurança Restrito?** Se você estiver desenvolvendo um formulário que exija segurança no nível de Domínio, o InfoPath exige que você publique o formulário em um local compartilhado para que os usuários possam abri-lo. Como os modelos de formulário só serão abertos no nível de segurança solicitado, os formulários abertos diretamente de uma mensagem de email não serão abertos se o InfoPath não puder conceder segurança no nível do Domínio. 
    
## <a name="benefits-of-using-signed-form-templates"></a>Benefícios do uso de modelos de formulário assinados

- Permite que o modelo de formulário seja aberto com segurança de Confiança Total.
    
- Evita que a mensagem de conflito de cache seja exibida se o formulário for movido para um novo local.
    
Além disso, se um modelo de formulário for assinado, você terá a vantagem extra da funcionalidade de atualização automática. Para saber mais, confira [Implantar modelos de formulário assinados do InfoPath](deploying-signed-infopath-form-templates.md).
  
### <a name="example-updating-domain-or-restricted-templates"></a>Exemplo: atualizar modelos de domínio ou restritos

O exemplo a seguir mostra como um modelo de formulário assinado e atualizado que solicita acesso de Domínio ou Restrito pode substituir uma cópia mais antiga: 
  
1. "A" envia um modelo de formulário assinado para "B".
    
2. "B" abre o modelo de formulário.
    
3. "A" atualiza o modelo de formulário (por exemplo, adiciona mais campos).
    
4. "A" envia um modelo de formulário atualizado para "B".
    
5. "B" abre o modelo de formulário atualizado.
    
### <a name="example-deploying-restricted-form-templates-on-an-extranet"></a>Exemplo: como implantar modelos de formulário restritos em uma extranet
  
1. Salve o modelo de formulário de Domínio em um site que executa o Microsoft SharePoint Foundation 2010.
    
2. Altere o nível de segurança do modelo de formulário para Restrito.
    
3. Salve o modelo de formulário em sua área de trabalho.
    
4. Remova a URL (necessário apenas se os usuários tiverem acesso ao local de publicação original).
    
5. Envie o formulário para os usuários em uma extranet.
    
6. Instrua os usuários a instalar o formulário.
    
7. Peça aos usuários para enviá-lo para você após o preenchimento.
    
8. Salve o formulário no site que está executando o SharePoint Foundation 2010 e vincule novamente o formulário usando a opção **Vincular documentos a esta biblioteca novamente** na página **Configurações da biblioteca de formulários**. 
    
## <a name="signature-verification-failure"></a>Falha na verificação da assinatura

Um modelo de formulário assinado que solicita acesso de confiança total não será aberto caso sua assinatura não puder ser autenticada. Essa verificação da assinatura pode falhar por um dos seguintes motivos:
  
- O certificado raiz não está no armazenamento de certificado raiz confiável.
    
- O certificado usado para assinar o modelo de formulário expirou.
    
- O certificado usado para assinar o modelo de formulário foi revogado.
    
- A assinatura no modelo de formulário está corrompida (uma indicação de que o modelo de formulário foi alterado depois de ser assinado).
    
Se um modelo de formulário assinado solicitar acesso Restrito ou de Domínio, o InfoPath não analisará ou verificará a assinatura, exceto para determinar se o modelo poderá ser atualizado automaticamente.
  
## <a name="infrastructure-registry-keys-for-form-migration-open-behavior"></a>Chaves do Registro de infraestrutura para comportamento de abertura de migração de formulário

Quando um usuário tenta abrir um formulário e o formulário é comparado a um modelo de formulário pela sua ID de formulário, o InfoPath exibirá uma mensagem de erro se o modelo de formulário tiver um nível de confiança de Domínio e o domínio não corresponder ao atributo *href* do formulário. Isso impede a abertura de formulários que não foram criados explicitamente usando o modelo de formulário. 
  
O InfoPath não permite que modelos de formulário com a mesma ID de formulário coexistam. Quatro chaves de registro adicionais ajudam os administradores de sistema a oferecer aos usuários a opção de permitir que o arquivo XML seja aberto em um modelo de formulário. Esse modelo também permite que os administradores definam o comportamento de abertura desejado para os formulários.
  
A tabela a seguir descreve as configurações padrão das chaves de registro. Se essas chaves do registro estiverem ausentes, o valor padrão especificado na tabela será aplicado.
  
Os valores Nomes correspondem às configurações de domínio do Internet Explorer. Esses valores determinam o comportamento de abertura dos formulários nessas zonas de segurança, bloqueando ou permitindo a abertura do formulário ou oferecendo ao usuário a opção de abrir o formulário.
  
|**Valor do nome**|**Bloquear**|**Interface do usuário**|**Permitir**|
|:-----|:-----|:-----|:-----|
|**Internet** <br/> |X  <br/> |||
|**Intranet** <br/> ||X  <br/> ||
|**Computador cliente** <br/> |||X  <br/> |
|**Site confiável** <br/> |||X  <br/> |
   
O caminho da chave de registro é `HKEY_CURRENT_USER\Software\Microsoft\Office\14.0\InfoPath\Open Behaviors`.

O comportamento de abertura do formulário é definido da seguinte forma:
  
- `Block [REG_DWORD = 0]`- Uma caixa de diálogo de erro com um botão Ajuda será exibida. O InfoPath não permitirá que o arquivo XML seja aberto quando o formulário estiver sendo executado na zona de segurança especificada e não corresponder ao domínio do modelo. 
    
- `User Interface [REG_DWORD = 1]`- A caixa de diálogo Sim/Não será exibida. O InfoPath solicitará que o usuário abra o arquivo XML no modelo de formulário quando o formulário estiver sendo executado na zona de segurança especificada e não corresponder ao domínio do modelo. 
    
- `Allow [REG_DWORD = 2]` - O arquivo XML será aberto sem erros ou caixas de diálogo de aviso. O InfoPath permitirá que o arquivo XML seja aberto quando o formulário estiver sendo executado na zona de segurança especificada e não corresponder ao domínio do modelo. 
    
Se um formulário for aberto em um modelo de formulário em execução no nível de segurança de Domínio, e o domínio de segurança do local "em cache" do modelo (ou seja, onde o formulário está armazenado em cache) e o atributo **href** do formulário não coincidirem, o InfoPath verificará o registro para definir o comportamento de abertura do formulário. O comportamento permitido será baseado na zona de segurança na qual o modelo está localizado (o valor *CachedFromLocation*). 
  
Por exemplo, se um formulário corresponder a um modelo de formulário baseado na ID do formulário, mas não no Caminho de Acesso, e o modelo de formulário estiver armazenado em cache em um local da Internet, o InfoPath mostrará uma caixa de diálogo de erro com um botão Ajuda.
  
> [!NOTE]
> Os formulários do InfoPath não serão abertos quando o domínio for um domínio Restrito do Internet Explorer. Portanto, não há chave de registro para Sites restritos do Internet Explorer. 
  

