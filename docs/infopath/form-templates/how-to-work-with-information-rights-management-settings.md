---
title: Trabalhar com configurações de gerenciamento de direitos de informação
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- gerenciamento de direitos de informação [InfoPath 2007], InfoPath 2007, gerenciamento de direitos de informação, IRM [InfoPath 2007]
localization_priority: Normal
ms.assetid: 4ad91898-b23e-4410-8839-a65259e53d37
description: 'Há dois tipos de configurações de gerenciamento de direitos de informação (IRM) disponíveis no Microsoft InfoPath: um para proteger o acesso a modelos de formulário do InfoPath e um para controlar o acesso a e as ações em dados de formulário contidos em formulários concluídos.'
ms.openlocfilehash: 6f7317cfdc4e6bfc89482e813b1670c8b8861a6b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420007"
---
# <a name="work-with-information-rights-management-settings"></a>Trabalhar com configurações de gerenciamento de direitos de informação

Há dois tipos de configurações de gerenciamento de direitos de informação (IRM) disponíveis no Microsoft InfoPath: um para proteger o acesso a modelos de formulário do InfoPath e um para controlar o acesso a e as ações em dados de formulário contidos em formulários concluídos.
  
> [!NOTE]
> A restrição de permissão só está disponível para modelos de formulário compatíveis com o editor do InfoPath. Modelos de formulário compatíveis com o navegador não oferecem suporte ao IRM. 
  
## <a name="adding-the-manage-credentials-command-to-the-quick-access-toolbar"></a>Adicionar o comando gerenciar credenciais à barra de ferramentas de acesso rápido

O comando **gerenciar credenciais** usado para trabalhar com as configurações de IRM ao criar um modelo de formulário não está disponível por padrão. Use as etapas a seguir para adicioná-lo à **barra de ferramentas de acesso rápido**.
  
### <a name="add-the-manage-credentials-command-to-the-quick-access-toolbar"></a>Adicionar o comando gerenciar credenciais à barra de ferramentas de acesso rápido

1.  Clique na seta na extremidade direita da barra de **ferramentas de acesso rápido** para abrir o menu **Personalizar barra de ferramentas de acesso rápido** e, em seguida, clique em **mais comandos**.
    
2. Na lista **escolher comandos de** , selecione **todos os comandos**.
    
3. Role para baixo na lista para **gerenciar credenciais**e clique em **Adicionar**.
    
4. Clique em **OK**.
    
Para obter mais informações sobre como usar o comando **gerenciar credenciais** e a caixa de diálogo de **permissão** no InfoPath, consulte o tópico "criar um modelo de formulário com permissão restrita" na ajuda do InfoPath. 
  
## <a name="the-irm-object-model"></a>O modelo de objeto do IRM

Use a classe de [permissão](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.aspx) para acessar as configurações de permissão userpermissioncollection e IRM que podem ser aplicadas a um formulário. [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.aspx) Para acessar o objeto **Permission** associado a um modelo de formulário, use a propriedade [Permission](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Permission.aspx) da [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) classe XmlForm. O objeto **Permission** retornado fornece acesso à coleção de objetos [UserPermission](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermission.aspx) associados ao modelo de formulário e a cada instância de formulário criada com esse modelo. 
  
O objeto **Permission** e seus métodos e propriedades estão disponíveis se as permissões são restritas no modelo de formulário ativo ou não. Use a propriedade [Enabled](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.Enabled.aspx) para determinar se um formulário tem permissões restritas. 
  
As permissões em um formulário são habilitadas de uma das seguintes maneiras usando propriedades e métodos da classe Permission:
  
A propriedade **Enabled** é definida como **true**.
  
A propriedade [DocumentAuthor](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.DocumentAuthor.aspx) está definida. 
  
A propriedade [RequestPermissionUrl](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.RequestPermissionUrl.aspx) está definida. 
  
A propriedade [StoreLicenses](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.StoreLicenses.aspx) é definida como **true** ou **false**.
  
O método [ApplyPolicy](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.ApplyPolicy.aspx) é chamado. 
  
> [!NOTE]
> Se o cliente Windows Rights Management não estiver instalado no computador de um usuário, o uso da classe **Permission** gerará uma exceção. 
  
Para trabalhar programaticamente com as configurações de IRM de usuários individuais em **** formulários, use as classes userpermissioncollection e UserPermission. **** 
  
Um **** objeto UserPermission associa um conjunto de permissões para o formulário atual com um único usuário e uma data de vencimento opcional. Use o método [Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.Add.aspx) da classe **** userpermissioncollection para adicionar e conceder a um usuário um conjunto de permissões no formulário atual. Use o método [Remove](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.Remove.aspx) da classe **** userpermissioncollection para remover um usuário e as permissões do usuário. Enquanto algumas permissões concedidas por meio da interface do usuário aplicam-se a todos os usuários, como a impressão e **** a data de expiração, você pode usar as classes UserPermission e userpermissioncollection para atribuí-las a cada usuário com por usuário **** datas de expiração. O modelo de objeto permite que os desenvolvedores enumerem configurações de permissão em um formulário e forneçam funcionalidade que permite que os usuários de formulários adicionem permissões ao formulário sem ter que usar o painel de tarefas **permissão de formulário** ou a caixa de diálogo de **permissão** . 
  
> [!NOTE]
> Não é possível aplicar permissões quando um formulário está no modo de visualização. Por esse motivo, todas as propriedades da classe de **permissão** são somente leitura quando um formulário está sendo visualizado. No modo de visualização, a propriedade **Enabled** sempre retornará **false**e, se o código tentar alterar essa configuração, um **System. Runtime. InteropServices. COMException** é gerado e o erro "a propriedade/método não está disponível na visualização Mode "será retornado. Da mesma forma, os métodos associados **** às classes UserPermission e userpermissioncollection também retornarão esta mensagem de erro quando usadas no modo de visualização. **** 
  
### <a name="overview-of-the-permission-class"></a>Visão geral da classe de permissão

A **** classe userpermissioncollection fornece as propriedades e um método a seguir. 
  
|**Nome**|**Descrição**|
|:-----|:-----|
|Método [ApplyPolicy](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.ApplyPolicy.aspx)  <br/> |Aplica uma política ao formulário usando um arquivo de modelo de política.  <br/> |
|Propriedade [DocumentAuthor](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.DocumentAuthor.aspx)  <br/> |Obtém ou define o autor do formulário atual como um endereço de email.  <br/> |
|Propriedade [Enabled](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.Enabled.aspx)  <br/> |Obtém ou define se as configurações de permissão representadas pelo objeto **Permission** estão habilitadas para o formulário atual.  <br/> |
|Propriedade [PermissionFromPolicy](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.PermissionFromPolicy.aspx)  <br/> |Obtém ou define se uma política de permissão foi aplicada ao formulário atual.  <br/> |
|Propriedade [PolicyDescription](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.PolicyDescription.aspx)  <br/> |Obtém uma descrição da política que foi aplicada ao formulário atual.  <br/> |
|[](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.PolicyName.aspx) Propriedade PolicyName  <br/> |Obtém o nome da política que foi aplicada ao formulário atual.  <br/> |
|Propriedade [RequestPermissionUrl](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.RequestPermissionUrl.aspx)  <br/> |Obtém ou define o arquivo, a URL ou o endereço de email a ser contatado para usuários que precisam de permissões adicionais no formulário atual.  <br/> |
|Propriedade [StoreLicenses](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.StoreLicenses.aspx)  <br/> |Obtém ou define se a licença do usuário para exibir o formulário atual deve ser armazenada em cache para permitir a exibição offline quando o usuário não puder se conectar a um servidor de gerenciamento de direitos.  <br/> |
|[](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.UserPermissions.aspx) Propriedade userpermissions  <br/> |Obtém um **** objeto userpermissioncollection para o formulário atual.  <br/> |
   
### <a name="overview-of-the-userpermissioncollection-class"></a>Visão geral da classe userPermissioncollection

A **** classe userpermissioncollection fornece as seguintes propriedades e métodos. 
  
|**Nome**|**Descrição**|
|:-----|:-----|
|Método [Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.Add.aspx) (+ 3 sobrecargas)  <br/> |Adiciona um novo usuário ao formulário atual, opcionalmente, especificando permissões e uma data de expiração.  <br/> |
|Método[Remover](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.Remove.aspx)  <br/> |Remove o **** objeto UserPermission com o **userid** especificado da coleção.  <br/> |
|Método [RemoveAll](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.RemoveAll.aspx)  <br/> |Remove todos **** os objetos UserPermission da coleção.  <br/> |
|Propriedade [Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.Count.aspx)  <br/> |Obtém o número de **** objetos UserPermission na coleção.  <br/> |
|Propriedade [Item](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.Item.aspx) (sobrecarga + 1)  <br/> |Obtém um **** objeto UserPermission.  <br/> |
   
### <a name="overview-of-the-userpermission-class"></a>Visão geral da classe userPermission

A **** classe UserPermission fornece as propriedades e um método a seguir. 
  
|**Nome**|**Descrição**|
|:-----|:-----|
|Método[Remover](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermission.Remove.aspx)  <br/> |Remove o objeto **UserPermission** atual das permissões do formulário.  <br/> |
|Propriedade [ExpirationDate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermission.ExpirationDate.aspx)  <br/> |Obtém ou define a data de vencimento opcional para as permissões no formulário atual atribuído ao usuário associado a uma instância da classe **UserPermission** .  <br/> |
|Propriedade [Permission](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermission.Permission.aspx)  <br/> |Obtém ou define um valor que representa as permissões no formulário atual atribuído ao usuário associado a uma instância da classe **UserPermission** .  <br/> |
|Propriedade [userid](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermission.UserId.aspx)  <br/> |Obtém o endereço de email do usuário cujas permissões no formulário atual são determinadas pelo objeto userPermission **** especificado.  <br/> |
   
### <a name="the-permissiontype-enumeration"></a>A Enumeração PermissionType

As permissões de um usuário são definidas ou lidas usando valores de enumeração do PermissionType. [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.PermissionType.aspx) 
  
|**Nome**|**Descrição**|
|:-----|:-----|
|**PermissionType. Change** <br/> |Permite que os usuários exibam, editem, copiem e salvem, mas não imprimam um formulário. Equivalente às permissões **ler**, **Editar**, **salvar**e **extrair** combinadas.  <br/> |
|**PermissionType. Edit** <br/> |Permite que o usuário edite o formulário.  <br/> |
|**PermissionType. Extract** <br/> |Permite que um usuário com a permissão de **leitura** Copie conteúdo no formulário.  <br/> |
|**PermissionType. FullControl** <br/> |Permite que o usuário adicione, altere e remova permissões para outros usuários de um formulário.  <br/> |
|**PermissionType. ObjectModel** <br/> |Permite que o usuário acesse o documento de formulário programaticamente por meio do modelo de objeto. Os usuários sem a permissão **ObjectModel** não podem usar o modelo de objeto para determinar suas próprias permissões.  <br/> |
|**PermissionType. Print** <br/> |Permite que o usuário imprima o formulário.  <br/> |
|**PermissionType. Read** <br/> |Permite que o usuário leia (exiba) o formulário. (As permissões de **leitura** e **Visualização** são equivalentes.)  <br/> |
|**PermissionType. Save** <br/> |Permite que o usuário salve o formulário.  <br/> |
|**PermissionType. View** <br/> |Permite que o usuário exiba (leia) o formulário. (As permissões de **leitura** e **Visualização** são equivalentes.)  <br/> |
   
### <a name="example"></a>Exemplo

No exemplo a seguir, clicar no controle **Button** Obtém o **** userpermissions para o formulário atual, adiciona e atribui um usuário ao nível de acesso Change e define uma data de expiração de dois dias a partir da data atual. 
  
```cs
public void CTRL1_Clicked(object sender, ClickedEventArgs e)
{
   string strExpirationDate = DateTime.Today.AddDays(2).ToString();
   DateTime dtExpirationDate = DateTime.Parse(strExpirationDate);
   this.Permission.UserPermissions.Add("someone@example.com", 
      PermissionType.Change, dtExpirationDate);
}
```

```vb
Public Sub CTRL1_Clicked(ByVal sender As Object, _
   ByVal e As ClickedEventArgs)
   Dim strExpirationDate As String = _
      DateTime.Today.AddDays(2).ToString()
   dtExpirationDate As DateTime = DateTime.Parse(strExpirationDate)
   Me.Permission.UserPermissions.Add("someone@example.com", _
      PermissionType.Change, dtExpirationDate)
End Sub
```


