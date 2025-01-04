# MkFractal Project

MkFractal is a Java-based application for generating and visualizing fractals. The project leverages Apache Commons libraries and Java Swing to create an interactive and customizable fractal rendering tool.

## Features

- Interactive fractal visualization with GUI.
- Modular design using Maven for dependency management.
- High-performance computation of complex numbers.
- Support for rendering and user interaction via Java Swing components.

## Requirements

- **Java**: Version 8 or higher
- **Apache Maven**: For building the project

## Installation

1. **Clone the repository**:
   ```bash
   git clone <repository-url>
   cd mkfractal
   ```

2. **Build the project**:
   ```bash
   mvn clean install
   ```

3. **Run the application**:
   ```bash
   java -jar target/mkfractal-1.0-SNAPSHOT.jar
   ```

## Project Structure

```plaintext
mkfractal/
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   ├── com/mycompany/mkfractal/
│   │   │   │   ├── Mkfractal.java
│   │   │   │   ├── NewJFrame.java
│   │   │   │   ├── NewJPanel.java
│   │   │   │   └── NewJFrame.form
│   │   │   └── org/apache/commons/numbers/complex/
│   │   │       ├── Complex.java
│   │   │       └── package-info.java
│   │   └── resources/
├── target/
│   ├── mkfractal-1.0-SNAPSHOT.jar
├── pom.xml
└── README.md
```

### Key Files

- **Mkfractal.java**: Main application entry point.
- **NewJFrame.java**: GUI implementation using Java Swing.
- **NewJPanel.java**: Custom rendering panel for fractal visualization.
- **pom.xml**: Maven configuration file for dependency management and build.

## Dependencies

The project uses the following dependencies:

- **Apache Commons Numbers (Complex)**:
  - JAR: `commons-numbers-complex-1.2.jar`
  - Documentation: `commons-numbers-complex-1.2-javadoc.jar`
  - Sources: `commons-numbers-complex-1.2-sources.jar`

Dependencies are managed via Maven and included in the `pom.xml` file.

## Fractal Structures

Fractals are intricate geometrical structures that exhibit self-similarity, meaning they look similar at different levels of magnification. This project focuses on rendering mathematical fractals, which are generated using complex number computations. Examples of fractal structures supported by the application include:

- **Mandelbrot Set**: A famous fractal defined by the iterative equation \( z_{n+1} = z_n^2 + c \), where \( z \) and \( c \) are complex numbers.
- **Julia Sets**: Derived from similar iterative equations but with a fixed complex parameter.

The rendering process involves:
1. Mapping each pixel on the screen to a point in the complex plane.
2. Iteratively applying the fractal equation to determine if the point escapes a defined boundary.
3. Coloring the pixel based on the number of iterations before escape, or if it remains bounded.

Users can explore these fractals interactively, zooming into regions of interest to reveal additional detail and complexity.

## Usage

1. Launch the application.
2. Use the interactive GUI to explore different fractal visualizations.
3. Modify rendering parameters directly in the interface.

## Development

### Adding Features
To extend the application:

1. **Add new rendering algorithms** in `NewJPanel.java`.
2. **Update the GUI** components in `NewJFrame.java`.
3. **Test and build** using Maven.

### Build Commands

- **Clean and Build**:
  ```bash
  mvn clean install
  ```

- **Run Tests**:
  ```bash
  mvn test
  ```

## License

This project is licensed under the Apache License 2.0. See the `LICENSE` file for details.

## Acknowledgments

- **Apache Commons Numbers** for providing the complex number library.
- **Java Swing** for the graphical user interface.

