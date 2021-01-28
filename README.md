<!-- This project created by imam abdul azis link : https://imamabdulazis.github.io/portofolio -->

# [Clean Architecture](https://blog.cleancoder.com/uncle-bob/2012/08/13/the-clean-architecture.html) Flutter Project


<p align="center">
<img alt="last commit" src="https://img.shields.io/github/last-commit/imamabdulazis/FlutterCleanArchitecture/main"/>
<img alt="last commit" src="https://app.codacy.com/project/badge/Grade/bc288b78ed0a4377b5e5ef72fdbad535"/>
<img alt="issue" src="https://img.shields.io/github/issues/imamabdulazis/FlutterCleanArchitecture?color=critical"/>
<img alt="last commit" src="https://img.shields.io/github/repo-size/imamabdulazis/FlutterCleanArchitecture?color=orange"/>
<img alt="last commit" src="https://img.shields.io/github/search/imamabdulazis/FlutterCleanArchitecture/flutter%20clean%20architecture?color=brightgreen"/>
<img alt="last commit" src="https://img.shields.io/github/downloads/imamabdulazis/FlutterCleanArchitecture/total"/>
</p>

<p>This is implementation clean architecture by Uncle Bob. We can implementation this project to make application with many module and component.
First we must prepare some library for supporting our project like injector, api consume like dio and many other library we must intall it.<br/>
In this case I made a facebook clone with rest API and you can clone it anytime and feel free to wait for my update app to make sure the app works properly.
</p>

## Getting Started.

![CleanArchitecture](https://user-images.githubusercontent.com/39134128/101283060-f3708c80-380a-11eb-94de-199f0fc01739.jpg)


> ### Installing
You can clone this library using :

```shell
git clone https://github.com/imamabdulazis/Flutter-Clean-Architectur-Bloc-RxDart-Dio.git
```

NOTE :
This project is using flutter version ```1.22.3``` and channel ```stable```
> ⚠️ If you are get any problem to this project please feel free to create issue

### Introduction
It is architecture based on the book and blog by Uncle Bob. It is a combination of concepts taken from the Onion Architecture and other architectures. The main focus of the architecture is separation of concerns and scalability. It consists of four main modules: App, Domain, Data, and Device.

<p>The Dependency Rule
Source code dependencies only point inwards. This means inward modules are neither aware of nor dependent on outer modules. However, outer modules are both aware of and dependent on inner modules. Outer modules represent the mechanisms by which the business rules and policies (inner modules) operate. The more you move inward, the more abstraction is present. The outer you move the more concrete implementations are present. Inner modules are not aware of any classes, functions, names, libraries, etc.. present in the outer modules. They simply represent rules and are completely independent from the implementations.</p>

## Layers
### Domain
<p>The Domain module defines the business logic of the application. It is a module that is independent from the development platform i.e. it is written purely in the programming language and does not contain any elements from the platform. The reason for that is that Domain should only be concerned with the business logic of the application, not with the implementation details. This also allows for easy migration between platforms, should any issues arise.</p>

### Contents of Domain
<h4>Domain is made up of several things.</h4>

### Entities
✅   Enterprise-wide business rules </br>
✅   Made up of classes that can contain methods </br>
✅   Business objects of the application </br>
✅   Used application-wide </br>
✅   Least likely to change when something in the application changes </br>

### Usecases
✅   Application-specific business rules </br>
✅   Encapsulate all the usecases of the application </br>
✅   Orchestrate the flow of data throughout the app </br>
✅   Should not be affected by any UI changes whatsoever </br>
✅   Might change if the functionality and flow of application change </br>

### Repositories
✅   Abstract classes that define the expected functionality of outer layers </br>
✅   Are not aware of outer layers, simply define expected functionality </br>
✅   E.g. The Login usecase expects a Repository that has login functionality </br>
✅   Passed to Usecases from outer layers </br>
✅   Domain represents the inner-most layer. Therefore, it the most abstract layer in the architecture. </br>

<br/>

### Library Requirement
<p>
We need some library to make our apps is more simple code and clean.
This is some library and you can click to install from pub dev.
</p> 


| Library                                                           | Usability                 |   Star    |
| :-----------------------------------------------------------------|:--------------------------|:---------:|
| [dartz](https://pub.dev/packages/dartz)                           | Data Handling             | [![Github Stars](https://img.shields.io/github/stars/spebbe/dartz?style=flat&logo=github&colorB=blue&label=stars)](https://github.com/spebbe/dartz) |
| [dio](https://pub.dev/packages/dio)                               | Http client               | [![Github Stars](https://img.shields.io/github/stars/flutterchina/dio?style=flat&logo=github&colorB=blue&label=stars)](https://github.com/felangel/bloc)    |
| [equatable](https://pub.dev/packages/equatable)                   | Getting data abstract     | [![Github Stars](https://img.shields.io/github/stars/felangel/equatable?style=flat&logo=github&colorB=blue&label=stars)](https://github.com/felangel/equatable)    |
| [flutter_hooks](https://pub.dev/packages/flutter_hooks)           | More simple code stateful | [![Github Stars](https://img.shields.io/github/stars/rrousselGit/flutter_hooks.svg?style=flat&logo=github&colorB=blue&label=stars)](https://github.com/rrousselGit/flutter_hooks)    |
| [flutter_bloc](https://pub.dev/packages/flutter_bloc)             | State management          | [![Github Stars](https://img.shields.io/github/stars/felangel/bloc.svg?style=flat&logo=github&colorB=blue&label=stars)](https://github.com/felangel/bloc)      |
| [get_it](https://pub.dev/packages/get_it)                         | Component Injector        | [![Github Stars](https://img.shields.io/github/stars/fluttercommunity/get_it?style=flat&logo=github&colorB=blue&label=stars)](https://github.com/fluttercommunity/get_it)     |
| [getx](https://pub.dev/packages/get)                              | Component handling        | [![Github Stars](https://img.shields.io/github/stars/jonataslaw/getx?style=flat&logo=github&colorB=blue&label=stars)](https://github.com/jonataslaw/getx)       |
| [pedantic](https://pub.dev/packages/pedantic)                     | Code formatting           | [![Github Stars](https://img.shields.io/github/stars/google/pedantic?style=flat&logo=github&colorB=blue&label=stars)](https://github.com/google/pedantic)     |
| [rxdart](https://pub.dev/packages/rxdart)                         | Data handling async       | [![Github Stars](https://img.shields.io/github/stars/reactiveX/rxdart?style=flat&logo=github&colorB=blue&label=stars)](https://github.com/ReactiveX/rxdart)     |
| [logger](https://pub.dev/packages/logger)                         | Beautiful terminal log    | [![Github Stars](https://img.shields.io/github/stars/google/pedantic?style=flat&logo=github&colorB=blue&label=stars)](https://github.com/google/pedantic)     |
| [shared_preferences](https://pub.dev/packages/shared_preferences) | Save data local storage   | [![Github Stars](https://img.shields.io/github/stars/flutter/plugins?style=flat&logo=github&colorB=blue&label=stars)](https://github.com/flutter/plugins)     |


## Code Explanation
<p>In some case we cannot implementation code by theary and just reading some tutorial without complete code. So here we go, I was build some code and improve some code from some tutorial and make it better I think :), I hope in this part can help us to make some simple Boilerplate.</p>

### Usecase

<p>
This is part more easy to handling some data error from network or other.
</p>

```dart
abstract class UseCase<Type, Params> {
  Stream<Either<Failure, Type>> build(Params params);

  Stream<Either<Failure, Type>> execute(Params params) {
    return build(params).onErrorResume((error) {
      print("error from streams : $error");
      Failure failure;

      if (error is Failure) {
        failure = error;
      } else if (error is DioError) {
        failure = ServerFailure(message: error.message);
      } else {
        failure = AnotherFailure(message: "$error");
      }

      return Stream.value(Left(failure));
    });
  }
}

class NoParams extends Equatable {
  @override
  List<Object> get props => [];
}
```

<br/>
<br/>

## Datasource Option 
<p>In this part we are enable to make option where data come from local or network</p>

>####Base Datasource (local or network or other)
```dart
abstract class BaseDataSourceFactory<T> {
  T createData(DataSourceState dataSourceState);
}

enum DataSourceState { network, local }
```

#### Datasource factory
```dart
class BindingDataSourceFactory
    extends BaseDataSourceFactory<BindingDataSource> {
  BindingRemote _bindingRemote;
  BindingLocal _bindingLocal;

  BindingDataSourceFactory({
    @required BindingRemote bindingRemote,
    @required BindingLocal bindingLocal,
  })  : _bindingRemote = bindingRemote,
        _bindingLocal = bindingLocal;

  @override
  BindingDataSource createData(DataSourceState dataSourceState) {
    switch (dataSourceState) {
      case DataSourceState.network:
        return _bindingRemote;
        break;
      case DataSourceState.local:
        return _bindingLocal;
      default:
        throw UnsupportedError(
            'DataSourceState $dataSourceState is not applicable in BindingDataSourceFactory');
    }
  }
}
```

<br/>

## Resource String Component
#### Handling component handling (i18n or Localization)
<p>
In this part we must handling component string and prepare if our project 
is using multiple language
</p>

```dart
//NOTE : base translation class
abstract class Translation {
  String get msgEmailInUse;
  String get msgInvalidCredentials;
  String get msgInvalidField;
  String get msgRequiredField;
  String get msgUnexpectedError;

  String get addAccount;
  String get confirmPassword;
  String get email;
  String get enter;
  String get login;
  String get name;
  String get password;
  String get reload;
  String get wait;
}

//NOTE : implement to language class

class ID implements Translation {
  String get msgEmailInUse => 'Email sudah digunakan';
  String get msgInvalidCredentials => 'Username atau password salah.';
  String get msgInvalidField => 'Bidang tidak valid';
  String get msgRequiredField => 'Kolom yang harus diisi';
  String get msgUnexpectedError => 'Ada yang salah. Silahkan coba lagi nanti.';

  String get addAccount => 'Buat sebuah akun';
  String get confirmPassword => 'Konfirmasi sandi';
  String get email => 'Email';
  String get enter => 'Gabung';
  String get login => 'Login';
  String get name => 'Nama';
  String get password => 'Kata sandi';
  String get reload => 'Muat ulang';
  String get wait => 'Tunggu...';
}


class R {
  static Translation string = ID();

  static void load(Locale locale) {
    switch (locale.toString()) {
      default:
        string = ID();
        break;
    }
  }
}

example calling :
    R.string.msgEmailInUse 
output :
    Email sudah digunakan

```



<br/>
<br/>

> ### Credit

This architecture is made with love:blush: and more things using great tutorials by great people, please visit this
project credit, thank you.

[Flutter Community](https://flutter.dev/community)<br/>
[Filled stack](https://www.filledstacks.com)<br/>
[Reso Coder](https://resocoder.com)<br/>
[Rezky Aulia Pratama](https://github.com/rezkyauliapratama)<br/>
[Ashish Rawat](https://dev.to/ashishrawat2911/handling-network-calls-and-exceptions-in-flutter-54me)
