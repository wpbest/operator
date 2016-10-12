# We use the microsoft/dotnet image as a starting point.
FROM microsoft/dotnet

# Install git
RUN apt-get install git -y

# Create a folder to clone our source code 
RUN mkdir git

# Set our working folder
WORKDIR git

# Clone the source code
RUN git clone https://github.com/wpbest/operator.git

# Set our working folder
WORKDIR operator/src/operator

# Expose port 5000 for the application.
EXPOSE 5000

# Restore nuget packages
RUN dotnet restore

# Start the application using dotnet!!!
ENTRYPOINT dotnet run