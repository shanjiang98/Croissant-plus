# Croissant-plus
Croissant is a framework using mutation testing to generate flaky mutants. Is is used in evaluating flaky test detection tools. You can check all data and details of Croissant at https://sites.google.com/view/croissant-website.

Croissant-plus is an extension of Croissant, can be adopted to different scenes such as micro service applications

## Requirements

- Ubuntu 22.04
- Java8
- Maven 3.6.3

## Dependencies

- Python 3.8+
- Pandas
- Matplotlib
- Tkinter
- BeautifulSoup4

## Running Croissant-plus framework

### Before you start

- Install all dependencies and meet all requirments.
- You can run the setup script by one command.
```
bash setup.sh
```

### Build the Mutation Testing Tools
Build the Croissant tools first, just run the build script by this command.
```
bash build.sh
```

### Run results for your projects

1. Generate the input projects, you can modify the projects.csv in this directory. This `projects.csv` contains 3 columns, which is `url`, `sha`, `JUnit Version`. For example,
```
https://github.com/apache/commons-cli,8adbf64def81ee3e812e802a398ef5afbbfc69ee,4
...
```

2. Run the tools with NOD mutation operaters on all of the projects, you can use this command.
```
bash runNOD.sh
```
Run the tools with OD mutation operaters you can use this command.
```
bash runOD.sh
```

3. Get the output of the tool, an `output` folder will be generated, for each run, a `TimeStamp1` folder will be generated which includes `logs`, `results`, `mutant` for each project
```
output
   ├── TimeStamp1
    │   ├── results
    │   ├── logs
    │   └── mutant
   ├── TimeStamp2 
    │   ├── results
    │   ├── logs
    │   └── mutant
    └── ...
```

