---
title: Níveis de segurança, implantação de email e modelos de formulário remotos
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7fc438ad-ae26-3632-3444-371537eaecb3
description: Microsoft InfoPath suporta movendo modelos de formulário de um local para outro, enviá-los como um anexo em uma mensagem de email e criação de modelos de formulário confiança total que estão assinados digitalmente ou instalados.
ms.openlocfilehash: ea0145eb45f6a03dc8637ba5ec1dc1c80d240006
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765707"
---
# <a name="security-levels-email-deployment-and-remote-form-templates"></a>Níveis de segurança, implantação de email e modelos de formulário remotos

Microsoft InfoPath suporta movendo modelos de formulário de um local para outro, enviá-los como um anexo em uma mensagem de email e criação de modelos de formulário confiança total que estão assinados digitalmente ou instalados.
  
## <a name="security-levels"></a>Níveis de segurança

Modelos de formulário podem ter um dos três níveis de segurança, dependendo de onde o formulário está localizado. Esses três níveis de segurança são descritos nas seções a seguir. 
  
### <a name="restricted"></a>Restricted

O nível de segurança restrito não permite qualquer comunicação fora o modelo de formulário. Esse nível de segurança é destinado a impedir a transmissão de dados do seu computador para um invasor mal-intencionado formulários prejudiciais. Ao executar neste modo de segurança, os seguintes recursos não funcionará:
  
- Painéis de tarefa de HTML  
- Consulta do SharePoint
- Envio do SharePoint
- Consulta de arquivo XML
- Consulta de banco de dados
- Envio de banco de dados
- Consulta à Web do serviço
- Envio de serviço Web
- Envio de código personalizado
- Envio de ambiente de hospedagem
- Controles ActiveX
- Funções
- Fluxo de trabalho do SharePoint
- Regras que abre um novo documento
- Código gerenciado
- Modo de exibição de impressão externo
- Imagens vinculadas
    
### <a name="domain"></a>Domínio

O nível de segurança de domínio restringe um formulário a um determinado domínio de Internet e suas permissões são impedidos as configurações do Internet Explorer para a zona onde o domínio está localizado. O formulário pode se comunicar com outras fontes de dados dentro de seu próprio domínio, mas geralmente não é permitido para recuperar dados de outros domínios, a menos que a zona permite a comunicação entre domínios. Este é o nível mínimo permitido para modelos de formulário compatíveis com navegador.
  
### <a name="full-trust"></a>Confiança total

O nível de segurança de confiança total permite que você execute um formulário com confiança total no computador onde o formulário será usado. Esse nível de segurança só pode ser usado quando você estiver trabalhando com um formulário localizado em um servidor que está assinado com uma assinatura que corresponde a um fornecedor de raiz confiável no seu computador, ou instalando o formulário. Ambos os métodos exigem que a configuração do atributo **requireFullTrust** como "yes". Usando essa configuração, o formulário pode acessar as chamadas de modelo de objeto, como para salvar arquivos e determinados avisos de segurança que aparecem quando você executa em um nível de segurança mais restritivo estão desabilitados. 
  
> [!NOTE]
> Todos os formulários gerados em designer do InfoPath têm um nível de segurança associado a eles. InfoPath abre formulários no seu nível de segurança associadas. Se o nível de segurança associado ao formulário for maior do que o nível de segurança que pode ser concedido a ele, o formulário não será aberto. 
  
A confiança total só pode ser definido para o nível de segurança instalado ou assinado modelos de formulário; Caso contrário, o nível de confiança máximo é de domínio. InfoPath não definirá um nível de segurança como confiança total automaticamente.
  
Formulários recebem níveis de segurança com base no local do qual o formulário é aberto.
  
## <a name="trust-levels"></a>Níveis de confiança

O nível mais alto de confiança que pode ser concedido a um modelo de formulário é determinado pelo aberto do local e outros códigos de verificação, conforme descrito na tabela a seguir. Os atributos listados na tabela (por exemplo, HTTP, UNC, *requireFullTrust*) são entradas que são usadas para determinar o nível de confiança que pode ser concedido a um formulário e aplicam-se aos formulários abertos no cliente do InfoPath. 
  
|Nível mais alto de confiança concedido|Confiança total|Computador cliente (em área restrita)|Intranet (em área restrita)|Internet (em área restrita)|Restricted|
|:-----|:-----:|:-----:|:-----:|:-----:|:-----:|
|**arquivo: Access caminho = aberto de local** <br/> |||X  <br/> |||
|**arquivo: Access caminho\<\>aberto de local ou caminho nenhum acesso (independentemente de onde o formulário provém)** <br/> |||||X  <br/> |
|**Aberta de local: Intranet HTTP ou HTTPS** <br/> |||X  <br/> |||
|**Aberta de local: Internet HTTP ou HTTPS** <br/> ||||X  <br/> ||
|**Abertos a partir de local: UNC** <br/> |||X  <br/> |||
|**Instalado o modelo (requireFullTrust = "yes")** <br/> |X  <br/> |||||
|**Instalado o modelo (requireFullTrust = "não")** <br/> ||X  <br/> ||||
|**Modelo de certificado de um fornecedor confiável** <br/> |X  <br/> |||||
|**Arquivos de formulário exportado** <br/> |||X  <br/> |||
   
## <a name="form-open-behavior"></a>Comportamento de abertura de formulário

Todos os arquivos de formulário abertos no InfoPath editor são vinculados por um conjunto de condições que determinam o nível de segurança no qual o formulário será aberto e se ela será aberta. Quando um formulário do InfoPath é aberto no editor, ele será aberto ou com um nível de segurança apropriados ou não será carregado. Se um formulário solicita um nível mais alto de segurança do que pode ser concedido (um formulário pode solicitar um nível de segurança específica usando o atributo **trustLevel** ou **requireFullTrust** ), ele não poderão carregar. Caso contrário, ele será carregado com o nível de segurança que ele solicita. Se o modelo de formulário não é permitido abrir com o nível de segurança solicitado, o usuário não será capaz de abrir o formulário e receberá uma mensagem de erro. 
  
A tabela a seguir descreve as condições exigidas para abrir um formulário em cada nível de segurança e o comportamento resultante quando o usuário tenta abrir o formulário.
  
|Editor aberta/falhar|Confiança total (requireFullTrust = "yes")|Relação de confiança de domínio (trustLevel = "Domínio" ou em branco)|Restrito (trustLevel = "Restrito")|
|:-----|:-----|:-----|:-----|
|**Confiáveis (certificado confiável ou instalado)** <br/> |Editor abre no nível de confiança total  <br/> |N/A  <br/> |N/A  <br/> |
|**Relação de confiança de domínio: Computador cliente** <br/> |Falha ao abrir  <br/> |Editor é aberto no nível do domínio  <br/> |Editor abre no nível restrito  <br/> |
|**Relação de confiança de domínio: Intranet** <br/> |Falha ao abrir  <br/> |Editor é aberto no nível do domínio  <br/> |Editor abre no nível restrito  <br/> |
|**Relação de confiança de domínio: Internet** <br/> |Falha ao abrir  <br/> |Editor é aberto no nível do domínio  <br/> |Editor abre no nível restrito  <br/> |
|**Restrito** <br/> |Falha ao abrir  <br/> |Falha ao abrir  <br/> |Editor abre no nível restrito  <br/> |
   
## <a name="specifying-a-security-level"></a>Especificar um nível de segurança

O criador de formulários do InfoPath seleciona automaticamente o nível de segurança apropriado (restrito ou domínio), com base nos recursos que você está usando no formulário. A configuração de segurança é tão restritiva sempre que possível, começando restrito, para ajudar a garantir um maior nível de proteção para você e seus dados. Os usuários podem substituir manualmente, essa configuração automatizado para selecionar um nível de segurança que é mais apropriado para o formulário seguindo estas etapas:
  
1. Clique na guia **arquivo** e clique em **Opções de formulário** , na guia **informações** . 
    
2. Na lista **categorias** , clique em **segurança e confiança**.
    
3. Desmarque o **determinar o nível de segurança automaticamente (recomendado)** caixa de seleção. 
    
4. Selecione o nível de segurança desejado.
    
## <a name="mail-deployment-and-browser-enabled-form-templates"></a>Implantação de email e modelos de formulário habilitados para navegador

InfoPath permite que você envie seus modelos de formulário como um anexo em uma mensagem de email e movê-los de um local para outro. Implantação de email é uma maneira fácil e eficaz para distribuir formulários para uso interno e também para implantar os formulários para usuários remotos.
  
Como alternativa, se você tiver o Microsoft SharePoint Server 2010 com o InfoPath Forms Services, você pode criar modelos de formulário que permitem aos usuários que não possuem o InfoPath instalado para preencher formulários em um navegador da Web.
  
## <a name="understanding-form-identity"></a>Noções básicas sobre a identidade do formulário

Todos os formulários do InfoPath designer são criados com uma identidade. Essas informações de identidade ajudam InfoPath associar formulários de modelos de formulário no cache e recuperar atualizações aos formulários quando são lançadas para um local compartilhado. Por padrão, o InfoPath cria duas identidades para modelos de formulário: uma identificação de formulário e um caminho de acesso. 
  
### <a name="form-id"></a>ID de formulário

A identificação do formulário é um identificador exclusivo com base em um prefixo, o nome do formulário e o namespace do formulário. O identificador deve ser um nome exclusivo que pode ser usado para associar corretamente os arquivos de formulário com o modelo de formulário associado no cache do computador cliente. A identificação do formulário é especificada como o atributo de nome (por exemplo, `name="urn:MyForm:MyCompany:Template1:myXSD-1583-78-G3V94-23-47"`) no arquivo de definição de formulário (. xsf). 
  
### <a name="access-path"></a>Caminho de acesso

O caminho de acesso é um identificador de local que é usado para determinar o local correto para o modelo de formulário e também o local para receber atualizações. Quando salva ou publicada, onde o modelo de formulário for salva ou publicado torna-se o caminho de acesso padrão. Cada vez que um formulário é aberto no computador cliente, o formulário tenta associar-se com um formulário em cache. Ele tentará fazer isso na seguinte ordem:
  
1. Procure por um modelo de formulário totalmente confiáveis com uma ID de formulário correspondente.
    
2. Procure um modelo de formulário no cache com um caminho de acesso correspondente.
    
3. Procure por um modelo de formulário no cache com uma ID de formulário correspondente.
    
Após correspondido, o formulário será aberto com o modelo de formulário associado. Em casos em que a correspondência foi feita com um caminho de acesso, o InfoPath usará o caminho de acesso para recuperar atualizações para o modelo de formulário. Esse método simplifica a administração de empresa, manutenção e atualização de formulários. Nos casos em que não é possível fazer a correspondência e o nível de confiança é o domínio, o formulário não será aberto. O caminho de acesso é especificado como o atributo **publishUrl** no arquivo de definição de formulário (. xsf). 
  
Assim como há duas propriedades de identificação para cada modelo de formulário, há um conjunto de heurística para determinar especificamente as entradas resultantes no cache, com base na condição de modelo de formulário (se ele tem um caminho de acesso, uma identificação de formulário ou ambos) e o estado de conexão de rede.
  
## <a name="designing-a-form-to-send-as-an-attachment-to-an-email-message"></a>Criação de um formulário para ser enviada como um anexo para uma mensagem de email

Todos os formulários que são criados no InfoPath designer podem ser enviados aos usuários como um anexo em uma mensagem de email. Implantação de email é uma maneira fácil e eficaz para distribuir formulários para uso interno e também para implantar os formulários para usuários remotos.
  
### <a name="to-mail-a-form-template-to-other-users"></a>Para um modelo de formulário de email para outros usuários

1. Clique na guia **arquivo** , clique em **Publicar**e, em seguida, clique no botão de **Email** . 
    
2. Preencher as duas próximas páginas do **Assistente de publicação** clicando em **próximo** para continuar depois de cada página e, em seguida, clique em **Publicar**.
    
3. Será exibida uma mensagem de email, permitindo que você preencha a lista de destinatários e quaisquer instruções adicionais que você pode ter para eles.
    
4. Depois de terminar, clique em **Enviar**. O formulário e o modelo de formulário serão anexados à mensagem.
    
## <a name="email-deployment-restricted-domain-and-full-trust-form-templates"></a>Implantação de email: restrito, domínio e modelos de formulário de confiança total

Implantação de email de modelos de formulário restrito permite formulários dinâmicos sem conexões de dados a ser aberto em qualquer lugar. Os destinatários podem abrir os modelos de formulário enviados como anexos de email diretamente do Microsoft Outlook 2010 ou de onde quer que o destinatário tenha salva o anexo. Além disso, o Outlook 2010 permite aos usuários editar formulários diretamente na mensagem.
  
Modelos de formulário com o nível de confiança de domínio devem ser abertos a partir de seu local publicado, mas publicando a uma lista de destinatários de email no Assistente de publicação, eles podem ser enviados como um anexo em uma mensagem de email. Quando o anexo é aberto, ele funciona como um link para o local publicado real do modelo. O modelo de formulário nesse local é o que realmente é aberto no editor do InfoPath.
  
Usando um modelo de formulário de nível de domínio enviado como um anexo de email se parece com usando qualquer outro tipo de documento; Por exemplo, uma pasta de trabalho do Microsoft Excel ou um documento do Microsoft Word. Um usuário pode basta clicar no formulário para abrir e usá-lo. Além disso, todos os benefícios das atualizações de nível de domínio estão disponíveis para os usuários.
  
Você pode enviar por email modelos de formulário que solicitam acesso de confiança total, mas esses modelos devem ser assinados ou que eles não poderão abrir. Modelos de formulário que está solicitando acesso domínio ou restrito não precisa estar conectado para ser enviada como um anexo de email. InfoPath não verifique ou verificar a assinatura, mesmo se o modelo for assinado, exceto para ver se ele pode ser atualizado automaticamente. Você pode assinar digitalmente um modelo de formulário do domínio ou restrito e ainda ter o recurso de atualização automática. Nesse caso, a assinatura digital impedirá quaisquer mensagens de conflito do cache que aparecem.
  
## <a name="sharing-forms-by-email-message-or-from-a-common-shared-location"></a>Compartilhamento de formulários por mensagem de email ou de um local compartilhado comuns

Determinadas perguntas devem ser consideradas quando você estiver criando um formulário que será implantado por mensagem de email.
  
- **Seu formulário ser atualizado regularmente?** Se você estiver desenvolvendo um formulário que deve ser atualizado regularmente, o formulário deverá ser publicado em um local compartilhado antes que sejam enviados para outros usuários. Essa prática permite atualizar o formulário pela publicação versões mais recentes para o local compartilhado, mas ele também permite que você distribuir imediatamente o modelo de formulário para usuários que podem não ter acesso ao local compartilhado. 
    
   Se um formulário for atualizado e, em seguida, distribuído pela mensagem de email, os usuários receberão uma mensagem de conflito de cache ao tentar abrir o novo formulário, se eles têm uma versão mais antiga armazenada no seu computador e o caminho de acesso foi alterada. O usuário deverá escolher qual versão que queiram usar. Mesmo se o formulário atualizado é o mesmo que aquele no computador do usuário, o usuário receberá uma mensagem de conflito de cache e ser solicitado a escolher qual cópia que queiram usar. A prática recomendada para usar no último caso é compartilhar o formulário a partir de um local compartilhado em vez disso.
    
- **Seu formulário acessar uma conexão de dados ou usar outros recursos que não tem suportados no nível de segurança restrito?** Se você estiver desenvolvendo um formulário que exige a segurança em nível de domínio, o InfoPath requer que você publique o formulário em um local compartilhado para os usuários poderão abri-lo. Porque os modelos de formulário serão aberto somente no nível de segurança que eles solicitam, formulários abertos a partir de uma mensagem de email não serão aberto se InfoPath não puder conceder a segurança no nível do domínio. 
    
## <a name="benefits-of-using-signed-form-templates"></a>Benefícios do uso de modelos de formulário assinado

- Ele permite que o modelo de formulário abrir com segurança de confiança total.
    
- Ela evita a mensagem de conflito do cache, se o formulário é movido para um novo local.
    
Além disso, se um modelo de formulário é assinado, você obterá o benefício adicional da funcionalidade de atualização automática. Para obter mais informações, consulte [Implantando modelos de formulário InfoPath assinado](deploying-signed-infopath-form-templates.md).
  
### <a name="example-updating-domain-or-restricted-templates"></a>Exemplo: Atualizando o domínio ou restritos modelos

O exemplo a seguir mostra como um modelo de formulário atualizado, assinado solicitando acesso domínio ou restrito pode sobrescrever uma cópia antiga: 
  
1. "A" envia um modelo de formulário assinado para "B".
    
2. "B" abre o modelo de formulário.
    
3. "A" atualiza o modelo de formulário (por exemplo, adiciona mais campos).
    
4. "A" envia o modelo de formulário atualizado para "B".
    
5. "B" abre o modelo de formulário atualizado.
    
### <a name="example-deploying-restricted-form-templates-on-an-extranet"></a>Exemplo: Modelos de formulário Implantando restritos em uma extranet
  
1. Salve o modelo de formulário do domínio em um site que está executando o Microsoft SharePoint Foundation 2010.
    
2. Altere o nível de segurança do modelo de formulário para restrito.
    
3. Salve o modelo de formulário em sua área de trabalho do computador.
    
4. Remova a URL (necessária somente se os usuários têm acesso ao original publicar local).
    
5. Envie o formulário para usuários em uma extranet.
    
6. Que os usuários a instalar o formulário.
    
7. Ter usuários enviar o formulário novamente para você após preenchê-lo.
    
8. Salve o formulário novamente ao site da Web que está executando o SharePoint Foundation 2010 e vincular novamente o formulário usando a opção **vincular novamente os documentos para essa biblioteca** na página **Definições da biblioteca de formulário** . 
    
## <a name="signature-verification-failure"></a>Falha de verificação da assinatura

Um modelo de formulário assinado que solicita acesso de confiança total, mas para o qual a assinatura não poderão ser autenticada não será aberto. Verificação da assinatura pode falhar por qualquer um dos seguintes motivos:
  
- O certificado raiz não está no repositório de certificados raiz confiáveis.
    
- O certificado que foi usado para assinar o modelo de formulário expirou.
    
- O certificado que foi usado para assinar o modelo de formulário foi revogado.
    
- A assinatura no modelo de formulário está corrompida (uma indicação de que o modelo de formulário foi alterado depois que ele foi conectada).
    
Se um modelo de formulário assinado solicitar acesso domínio ou restrito, o InfoPath não verifique ou verificar a assinatura exceto to determinar se o modelo pode ser atualizado automaticamente.
  
## <a name="infrastructure-registry-keys-for-form-migration-open-behavior"></a>Comportamento de abertura de chaves de registro de infraestrutura para migração de formulário

Quando um usuário tenta abrir um formulário, e o formulário é correspondido contra um modelo de formulário, por sua ID de formulário, o InfoPath exibirá uma mensagem de erro se o modelo de formulário tem um nível de confiança de domínio e o domínio não coincide com o atributo *href* do formulário. Isso impede que os formulários sejam abertos que não foram explicitamente criados usando o modelo de formulário. 
  
InfoPath não permite que os modelos de formulário com a mesma ID de formulário para coexistir. Quatro chaves do registro adicionais ajudam os administradores de sistema dar aos usuários a opção de se você deseja permitir o arquivo XML para abrir em relação a um modelo de formulário. Este modelo também permite aos administradores definir o comportamento de abertura querem para formulários.
  
A tabela a seguir descreve as configurações padrão para as chaves do registro. Se essas chaves do registro estiverem ausentes, o valor padrão especificado na tabela será imposto.
  
Os valores de nome correspondem às configurações de domínio do Internet Explorer. Esses valores determinam o comportamento de abertura de formulário nessas zonas de segurança, o bloqueio ou permitindo a abertura do formulário ou dando ao usuário a opção para abrir o formulário.
  
|**Valor de nome**|**Bloquear**|**Interface do usuário**|**Permitir**|
|:-----|:-----|:-----|:-----|
|**Internet** <br/> |X  <br/> |||
|**Intranet** <br/> ||X  <br/> ||
|**Computador cliente** <br/> |||X  <br/> |
|**Site confiável** <br/> |||X  <br/> |
   
É o caminho da chave do registro `HKEY_CURRENT_USER\Software\Microsoft\Office\14.0\InfoPath\Open Behaviors`.

O comportamento de abertura do formulário é definido da seguinte maneira:
  
- `Block [REG_DWORD = 0]`-Uma caixa de diálogo de erro com um botão Ajuda será exibida. InfoPath não permitirá que o arquivo XML abrir quando o formulário está em execução na zona de segurança especificado e não corresponder ao domínio de modelo. 
    
- `User Interface [REG_DWORD = 1]`-O Sim/caixa de diálogo não será exibida. InfoPath solicitará ao usuário para abrir o arquivo XML em relação ao modelo de formulário quando o formulário está em execução na zona de segurança especificado e não corresponder ao domínio de modelo. 
    
- `Allow [REG_DWORD = 2]`-O arquivo XML será aberto sem um erro ou o diálogo de aviso. InfoPath permitirá que o arquivo XML abrir quando o formulário está em execução na zona de segurança especificado e não corresponder ao domínio de modelo. 
    
Se um formulário é aberto em relação a um modelo de formulário em execução no nível de segurança do domínio e o domínio de segurança do modelo de "armazenados em cache de" local (ou seja, onde o formulário é armazenado em cache do) e o atributo de **href** do formulário não coincidirem, o InfoPath verificarão o Registro para definir o comportamento de abertura do formulário. Permitido comportamento será baseado na zona de segurança no qual o modelo está localizado (o valor de *CachedFromLocation* ). 
  
Por exemplo, quando um formulário corresponde a um modelo de formulário com base na ID de formulário, mas não no caminho de acesso e o modelo de formulário é armazenado em cache a partir de um local da Internet, o InfoPath mostrará uma caixa de diálogo de erro com um botão Ajuda.
  
> [!NOTE]
> Os formulários do InfoPath não serão aberto quando o domínio é um domínio de Internet Explorer restrito; Portanto, não há nenhuma chave do registro para Sites restritos do Internet Explorer. 
  

