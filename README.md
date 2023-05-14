import java.util.ArrayList;
import java.util.List;

public class AgricultureAdvisoryApp {

    private static final List<String> crops = new ArrayList<>();

    static {
        crops.add("corn");
        crops.add("soybeans");
        crops.add("wheat");
        crops.add("rice");
        crops.add("cotton");
        crops.add("vegetables");
        crops.add("fruits");
    }

    public static void main(String[] args) {
        System.out.println("Welcome to the Agriculture Advisory App!");

        // Get the user's input
        System.out.print("What crop would you like to learn about? ");
        String crop = System.console().readLine();

        // Check if the crop is in the list
        if (!crops.contains(crop)) {
            System.out.println("Sorry, I don't have any information on that crop.");
            System.exit(0);
        }

        // Get the user's location
        System.out.print("What is your location? ");
        String location = System.console().readLine();

        // Get the weather forecast for the user's location
        String weatherForecast = getWeatherForecast(location);

        // Get the latest news about the crop
        String news = getLatestNews(crop);

        // Print the advisory
        System.out.println("Here is the advisory for " + crop + ":");
        System.out.println("* Weather forecast: " + weatherForecast);
        System.out.println("* Latest news: " + news);
    }

    private static String getWeatherForecast(String location) {
        // TODO: Get the weather forecast for the user's location
        return "Sunny with a high of 75 degrees Fahrenheit.";
    }

    private static String getLatestNews(String crop) {
        // TODO: Get the latest news about the crop
        return "The price of corn is expected to rise in the coming months.";
    }
}
